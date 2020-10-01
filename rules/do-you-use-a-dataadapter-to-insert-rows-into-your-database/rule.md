---
type: rule
title: Do you use a DataAdapter to insert rows into your database?
uri: do-you-use-a-dataadapter-to-insert-rows-into-your-database
created: 2009-05-05T05:30:52.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 17
  title: Ryan Tee

---

There are 5 common methods of inserting rows into your database:<br> 
1. Use SqlCommand with an SQL INSERT statement and parameters:


```
public void SQLInsert(string customerID, string companyName, string contactName){    SqlConnection sqlcon = new SqlConnection();    sqlcon.ConnectionString = "Persist Security Info=False;                Integrated Security=SSPI;database=northwindJV;               server=(local);Connect Timeout=5";    SqlCommand sqlcmd = new SqlCommand();    sqlcmd.CommandText = "INSERT Customers(CustomerID, CompanyName,                 ContactName) VALUES(@CustomerID, @CompanyName, @ContactName)";    sqlcmd.Connection = sqlcon;    sqlcmd.Parameters.Add("@CustomerID", customerID);    sqlcmd.Parameters.Add("@CompanyName", companyName);    sqlcmd.Parameters.Add("@ContactName", contactName);        ... // for all columns         try    {        sqlcon.Open();        MessageBox.Show("The number of records updated was: "         + sqlcmd.ExecuteNonQuery().ToString());    }    finally   {        sqlcon.Close();   }}
```

     Figure: Inserting rows using INSERT     This approach has two problems - the SQL is inline in the code, and if the database schema is changed, INSERT statement will have to be manually updated.
2. Use SqlCommand and a stored procedure on the SQL Server:


```
public void SPInsert(string firstName, string surname){        SqlConnection sqlcon = new SqlConnection();        sqlcon.ConnectionString = "Persist Security Info=False;Integrated Security=SSPI; database=northwind;server=mySQLServer;Connect Timeout=30";        SqlCommand sqlcmd = new SqlCommand();        sqlcmd.CommandText = "proc_InsertCustomer";        sqlcmd.CommandType = CommandType.StoredProcedure;        sqlcmd.Connection = sqlcon;        sqlcmd.Parameters.Add("@firstName", firstName);        sqlcmd.Parameters.Add("@surname", surname);        ... // for all columns        try        {                sqlcon.Open();                sqlcmd.ExecuteNonQuery();        }        finally        {                sqlcon.Close();        }}
```

     Figure: Inserting rows using SqlCommand and a stored procedure on the SQL Server     This method is better because the SQL is not mixed up with the code (it is in a stored procedure), but it will still break if the database schema is changed, and the all of the parameters to the stored procedure have to be added manually.
3. Use DataAdapter with SQL INSERT statement, then use DataApdater.Update (strongly-typed-dataset)


```
public void DASQLInsert(string firstName, string surname){        SqlConnection sqlcon = new SqlConnection();        sqlcon.ConnectionString = "Persist Security Info=False; Integrated Security=SSPI; database=northwind; server=mySQLServer;Connect Timeout=30";        SqlCommand sqlcmd = new SqlCommand();        sqlcmd.CommandText = "INSERT Customers(firstName, surname)                   VALUES(@firstName, @surname)";        sqlcmd.Connection = sqlcon;        SqlDataAdapter sqladp = new SqlDataAdapter();        sqladp.InsertCommand = sqlcmd;            NorthWindCustomer dst = new NorthWindCustomer();        NorthWindCustomer.CustomerRow row = dst.Customer.NewCustomerRow();        row.FirstName = firstName;        row.Surname = surname;        dst.Customer.AddCustomerRow(row);        try        {                slqcon.Open();                sqladp.Update(dst);        }        finally        {                  sqlcon.Close();        }}
```

      Figure: Inserting rows using DataAdapter with SQL INSERT statement, then use DataApdater.Update     In this example, the SQL is mixed up with the .NET code, and has to be manually updated if the database schema is changed. However, the strongly typed DataSet automatically updates when the database schema changes.
4. Use DataAdapter with a stored procedure for INSERT, then use DataAdapter.Update (strongly-typed-dataset)


```
public void DASPInsert(string firstName, string surname){        SqlConnection sqlcon = new SqlConnection();        sqlcon.ConnectionString = "Persist Security Info=False;                  Integrated Security=SSPI; database=northwind;                  server=mySQLServer;Connect Timeout=30";        SqlCommand sqlcmd = new SqlCommand();        sqlcmd.CommandText = "proc_InsertCustomer";        sqlcmd.CommandType = CommandType.StoredProcedure;        sqlcmd.Connection = sqlcon;        SqlDataAdapter sqladp = new SqlDataAdapter();        sqladp.InsertCommand = sqlcmd;        NorthWindCustomer dst = new NorthWindCustomer();        NorthWindCustomer.CustomerRow row = dst.Customer.NewCustomerRow();        row.FirstName = firstName;        row.Surname = surname;        dst.Customer.AddCustomerRow(row);            try        {                sqlcon.Open();                sqladp.Update(dst);        }        catch        {                MessageBox.Show(                      "Unable to open connection.",                      "Error", MessageBoxButtons.OK, MessageBoxIcon.Error);        }        finally        {                sqlcon.Close();        }}
```

     Figure: Inserting rows using DataAdapter with a stored procedure for INSERT, then use DataAdapter.Update (strongly-typed-dataset) - best for SQL Server     This is the best approach for Microsoft SQL Server. The parameters for the stored procedure are automatically generated and the strongly typed dataset updates when the database schema changes.
5. Use DataAdapter with SQL SELECT statement, then use command builder to automatically create INSERT, UPDATE and DELETE statements as required. Then use DataAdapter.Update (strongly-typed-dataset).


```
public void DACmdb(string firstName, string surname){        SqlConnection sqlcon = new SqlConnection();        sqlcon.ConnectionString = "Persist Security Info=False;                  Integrated Security=SSPI; database=northwind;                  server=mySQLServer;Connect Timeout=30";        SqlCommand sqlcmd = new SqlCommand();        sqlcmd.CommandText = "SELECT firstName, surname FROM Customers";        sqlcmd.Connection = sqlcon;        SqlDataAdapter sqladp = new SqlDataAdapter();        sqladp.SelectCommand = sqlcmd;        SqlCommandBuilder cmdb = new SqlCommandBuilder(adp);            NorthWindCustomer dst = new NorthWindCustomer();        NorthWindCustomer.CustomerRow row = dst.Customer.NewCustomerRow();        row.FirstName = firstName;        row.Surname = surname;        dst.Customer.AddCustomerRow(row);            try        {                sqlcon.Open();                sqladp.Update(dst);        }        catch        {                MessageBox.Show(                       "Unable to open connection.",                       "Error", MessageBoxButtons.OK, MessageBoxIcon.Error);        }        finally        {                sqlcon.Close();        }}
```

     Figure: Inserting rows using DataAdapter with SQL SELECT statement, then use command builder to automatically create INSERT, UPDATE and DELETE - best for SQL Server    This approach is the best approach for Jet (Access) databases, as stored procedures in Access are difficult to implement and unreliable. The INSERT statement is automatically generated by .NET and the strongly typed databases update when the database schema is changed.
