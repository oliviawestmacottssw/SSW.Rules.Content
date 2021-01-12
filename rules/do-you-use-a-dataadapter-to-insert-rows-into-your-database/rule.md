---
type: rule
archivedreason: 
title: Do you use a DataAdapter to insert rows into your database?
guid: 75a90696-0dce-4dae-a37c-6dedcd62d08a
uri: do-you-use-a-dataadapter-to-insert-rows-into-your-database
created: 2009-05-05T05:30:52.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
- title: Ryan Tee
  url: https://ssw.com.au/people/ryan-tee
related: []
redirects: []

---

There are 5 common methods of inserting rows into your database:  
<!--endintro-->

1. Use SqlCommand with an SQL INSERT statement and parameters:


```
public void SQLInsert(string customerID, string companyName, string contactName)<br>{<br>    SqlConnection sqlcon = new SqlConnection();<br>    sqlcon.ConnectionString = "Persist Security Info=False; <br>               Integrated Security=SSPI;database=northwindJV;<br>               server=(local);Connect Timeout=5";<br>    SqlCommand sqlcmd = new SqlCommand();<br>    sqlcmd.CommandText = "INSERT Customers(CustomerID, CompanyName, <br>                ContactName) VALUES(@CustomerID, @CompanyName, @ContactName)";<br>    sqlcmd.Connection = sqlcon;<br>    sqlcmd.Parameters.Add("@CustomerID", customerID);<br>    sqlcmd.Parameters.Add("@CompanyName", companyName);<br>    sqlcmd.Parameters.Add("@ContactName", contactName);<br>    <br>    ... // for all columns<br>    <br>     try<br>    {<br>        sqlcon.Open();<br>        MessageBox.Show("The number of records updated was: " <br>        + sqlcmd.ExecuteNonQuery().ToString());<br>    }<br>    finally<br>   {<br>        sqlcon.Close();<br>   }<br>}
```

     Figure: Inserting rows using INSERT<br>        This approach has two problems - the SQL is inline in the code, and if the database schema is changed, INSERT statement will have to be manually updated.
2. Use SqlCommand and a stored procedure on the SQL Server:


```
public void SPInsert(string firstName, string surname)<br>{<br>        SqlConnection sqlcon = new SqlConnection();<br>        sqlcon.ConnectionString = "Persist Security Info=False;Integrated Security=SSPI; database=northwind;server=mySQLServer;Connect Timeout=30";<br>        SqlCommand sqlcmd = new SqlCommand();<br>        sqlcmd.CommandText = "proc_InsertCustomer";<br>        sqlcmd.CommandType = CommandType.StoredProcedure;<br>        sqlcmd.Connection = sqlcon;<br>        sqlcmd.Parameters.Add("@firstName", firstName);<br>        sqlcmd.Parameters.Add("@surname", surname);<br>        ... // for all columns<br>        try<br>        {<br>                sqlcon.Open();<br>                sqlcmd.ExecuteNonQuery();<br>        }<br>        finally<br>        {<br>                sqlcon.Close();<br>        }<br>}
```

     Figure: Inserting rows using SqlCommand and a stored procedure on the SQL Server<br>        This method is better because the SQL is not mixed up with the code (it is in a stored procedure), but it will still break if the database schema is changed, and the all of the parameters to the stored procedure have to be added manually.
3. Use DataAdapter with SQL INSERT statement, then use DataApdater.Update (strongly-typed-dataset)


```
public void DASQLInsert(string firstName, string surname)<br>{<br>        SqlConnection sqlcon = new SqlConnection();<br>        sqlcon.ConnectionString = "Persist Security Info=False; Integrated Security=SSPI; database=northwind; server=mySQLServer;Connect Timeout=30";<br>        SqlCommand sqlcmd = new SqlCommand();<br>        sqlcmd.CommandText = "INSERT Customers(firstName, surname) <br>                  VALUES(@firstName, @surname)";<br>        sqlcmd.Connection = sqlcon;<br>        SqlDataAdapter sqladp = new SqlDataAdapter();<br>        sqladp.InsertCommand = sqlcmd;<br>    <br>        NorthWindCustomer dst = new NorthWindCustomer();<br>        NorthWindCustomer.CustomerRow row = dst.Customer.NewCustomerRow();<br>        row.FirstName = firstName;<br>        row.Surname = surname;<br>        dst.Customer.AddCustomerRow(row);<br>        try<br>        {<br>                slqcon.Open();<br>                sqladp.Update(dst);<br>        }<br>        finally<br>        {  <br>                sqlcon.Close();<br>        }<br>}
```

      Figure: Inserting rows using DataAdapter with SQL INSERT statement, then use DataApdater.Update<br>        In this example, the SQL is mixed up with the .NET code, and has to be manually updated if the database schema is changed. However, the strongly typed DataSet automatically updates when the database schema changes.
4. Use DataAdapter with a stored procedure for INSERT, then use DataAdapter.Update (strongly-typed-dataset)


```
public void DASPInsert(string firstName, string surname)<br>{<br>        SqlConnection sqlcon = new SqlConnection();<br>        sqlcon.ConnectionString = "Persist Security Info=False;<br>                  Integrated Security=SSPI; database=northwind;<br>                  server=mySQLServer;Connect Timeout=30";<br>        SqlCommand sqlcmd = new SqlCommand();<br>        sqlcmd.CommandText = "proc_InsertCustomer";<br>        sqlcmd.CommandType = CommandType.StoredProcedure;<br>        sqlcmd.Connection = sqlcon;<br>        SqlDataAdapter sqladp = new SqlDataAdapter();<br>        sqladp.InsertCommand = sqlcmd;<br>        NorthWindCustomer dst = new NorthWindCustomer();<br>        NorthWindCustomer.CustomerRow row = dst.Customer.NewCustomerRow();<br>        row.FirstName = firstName;<br>        row.Surname = surname;<br>        dst.Customer.AddCustomerRow(row);<br>    <br>        try<br>        {<br>                sqlcon.Open();<br>                sqladp.Update(dst);<br>        }<br>        catch<br>        {<br>                MessageBox.Show(<br>                      "Unable to open connection.",<br>                      "Error", MessageBoxButtons.OK, MessageBoxIcon.Error);<br>        }<br>        finally<br>        {<br>                sqlcon.Close();<br>        }<br>}
```

     Figure: Inserting rows using DataAdapter with a stored procedure for INSERT, then use DataAdapter.Update (strongly-typed-dataset) - best for SQL Server<br>        This is the best approach for Microsoft SQL Server. The parameters for the stored procedure are automatically generated and the strongly typed dataset updates when the database schema changes.
5. Use DataAdapter with SQL SELECT statement, then use command builder to automatically create INSERT, UPDATE and DELETE statements as required. Then use DataAdapter.Update (strongly-typed-dataset).


```
public void DACmdb(string firstName, string surname)<br>{<br>        SqlConnection sqlcon = new SqlConnection();<br>        sqlcon.ConnectionString = "Persist Security Info=False;<br>                  Integrated Security=SSPI; database=northwind;<br>                  server=mySQLServer;Connect Timeout=30";<br>        SqlCommand sqlcmd = new SqlCommand();<br>        sqlcmd.CommandText = "SELECT firstName, surname FROM Customers";<br>        sqlcmd.Connection = sqlcon;<br>        SqlDataAdapter sqladp = new SqlDataAdapter();<br>        sqladp.SelectCommand = sqlcmd;<br>        SqlCommandBuilder cmdb = new SqlCommandBuilder(adp);<br>    <br>        NorthWindCustomer dst = new NorthWindCustomer();<br>        NorthWindCustomer.CustomerRow row = dst.Customer.NewCustomerRow();<br>        row.FirstName = firstName;<br>        row.Surname = surname;<br>        dst.Customer.AddCustomerRow(row);<br>    <br>        try<br>        {<br>                sqlcon.Open();<br>                sqladp.Update(dst);<br>        }<br>        catch<br>        {<br>                MessageBox.Show(<br>                       "Unable to open connection.",<br>                       "Error", MessageBoxButtons.OK, MessageBoxIcon.Error);<br>        }<br>        finally<br>        {<br>                sqlcon.Close();<br>        }<br>}
```

     Figure: Inserting rows using DataAdapter with SQL SELECT statement, then use command builder to automatically create INSERT, UPDATE and DELETE - best for SQL Server<br>        This approach is the best approach for Jet (Access) databases, as stored procedures in Access are difficult to implement and unreliable. The INSERT statement is automatically generated by .NET and the strongly typed databases update when the database schema is changed.
