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


There are 5 common methods of inserting rows into your database&#58;

<br><excerpt class='endintro'></excerpt><br>

  <ol>
    <li>
    <p>Use SqlCommand with an SQL INSERT statement and parameters&#58;</p>
    <dl class="goodCode">
        <dt style="width&#58;95.47%;height&#58;516px;">
        <pre>public void SQLInsert(string customerID, string companyName, string contactName)<br>&#123;<br>    SqlConnection sqlcon = new SqlConnection();<br>    sqlcon.ConnectionString = &quot;Persist Security Info=False; <br>               Integrated Security=SSPI;database=northwindJV;<br>               server=(local);Connect Timeout=5&quot;;<br>    SqlCommand sqlcmd = new SqlCommand();<br>    sqlcmd.CommandText = &quot;INSERT Customers(CustomerID, CompanyName, <br>                ContactName) VALUES(@CustomerID, @CompanyName, @ContactName)&quot;;<br>    sqlcmd.Connection = sqlcon;<br>    sqlcmd.Parameters.Add(&quot;@CustomerID&quot;, customerID);<br>    sqlcmd.Parameters.Add(&quot;@CompanyName&quot;, companyName);<br>    sqlcmd.Parameters.Add(&quot;@ContactName&quot;, contactName);<br>    <br>    ... // for all columns<br>    <br>    &#160;try<br>    &#123;<br>        sqlcon.Open();<br>        MessageBox.Show(&quot;The number of records updated was&#58; &quot; <br>        + sqlcmd.ExecuteNonQuery().ToString());<br>    &#125;<br>    finally<br>   &#123;<br>        sqlcon.Close();<br>   &#125;<br>&#125;</pre>
        </dt>
        <dd>&#160;&#160;&#160;&#160; Figure&#58; Inserting rows using INSERT </dd>
    </dl>
    <p>This approach has two problems - the SQL is inline in the code, and if the database schema is changed, INSERT statement will have to be manually updated.</p>
    </li>
    <li>
    <p>Use SqlCommand and a stored procedure on the SQL Server&#58;</p>
    <dl class="goodCode">
        <dt style="width&#58;92.44%;height&#58;443px;">
        <pre>public void SPInsert(string firstName, string surname)<br>&#123;<br>    &#160;&#160;&#160;&#160;SqlConnection sqlcon = new SqlConnection();<br>    &#160;&#160;&#160;&#160;sqlcon.ConnectionString = &quot;Persist Security Info=False;Integrated Security=SSPI; database=northwind;server=mySQLServer;Connect Timeout=30&quot;;<br>    &#160;&#160;&#160;&#160;SqlCommand sqlcmd = new SqlCommand();<br>    &#160;&#160;&#160;&#160;sqlcmd.CommandText = &quot;proc_InsertCustomer&quot;;<br>    &#160;&#160;&#160;&#160;sqlcmd.CommandType = CommandType.StoredProcedure;<br>    &#160;&#160;&#160;&#160;sqlcmd.Connection = sqlcon;<br>    &#160;&#160;&#160;&#160;sqlcmd.Parameters.Add(&quot;@firstName&quot;, firstName);<br>    &#160;&#160;&#160;&#160;sqlcmd.Parameters.Add(&quot;@surname&quot;, surname);<br>    &#160;&#160;&#160;&#160;... // for all columns<br>    &#160;&#160;&#160;&#160;try<br>    &#160;&#160;&#160;&#160;&#123;<br>        &#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;sqlcon.Open();<br>        &#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;sqlcmd.ExecuteNonQuery();<br>    &#160;&#160;&#160;&#160;&#125;<br>    &#160;&#160;&#160;&#160;finally<br>    &#160;&#160;&#160;&#160;&#123;<br>        &#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;sqlcon.Close();<br>    &#160;&#160;&#160;&#160;&#125;<br>&#125;</pre>
        </dt>
        <dd>&#160;&#160;&#160;&#160; Figure&#58; Inserting rows using SqlCommand and a stored procedure on the SQL Server </dd>
    </dl>
    <p>This method is better because the SQL is not mixed up with the code (it is in a stored procedure), but it will still break if the database schema is changed, and the all of the parameters to the stored procedure have to be added manually.</p>
    </li>
    <li>
    <p>Use DataAdapter with SQL INSERT statement, then use DataApdater.Update (strongly-typed-dataset)</p>
    <dl class="goodCode">
        <dt style="overflow-x&#58;scroll;width&#58;92.76%;height&#58;533px;">
        <pre style="padding-left&#58;15px;">public void DASQLInsert(string firstName, string surname)<br>&#123;<br>    &#160;&#160;&#160;&#160;SqlConnection sqlcon = new SqlConnection();<br>    &#160;&#160;&#160;&#160;sqlcon.ConnectionString = &quot;Persist Security Info=False; Integrated Security=SSPI; database=northwind; server=mySQLServer;Connect Timeout=30&quot;;<br>    &#160;&#160;&#160;&#160;SqlCommand sqlcmd = new SqlCommand();<br>    &#160;&#160;&#160;&#160;sqlcmd.CommandText = &quot;INSERT Customers(firstName, surname) <br>                  VALUES(@firstName, @surname)&quot;;<br>    &#160;&#160;&#160;&#160;sqlcmd.Connection = sqlcon;<br>    &#160;&#160;&#160;&#160;SqlDataAdapter sqladp = new SqlDataAdapter();<br>    &#160;&#160;&#160;&#160;sqladp.InsertCommand = sqlcmd;<br>    <br>    &#160;&#160;&#160;&#160;NorthWindCustomer dst = new NorthWindCustomer();<br>    &#160;&#160;&#160;&#160;NorthWindCustomer.CustomerRow row = dst.Customer.NewCustomerRow();<br>    &#160;&#160;&#160;&#160;row.FirstName = firstName;<br>    &#160;&#160;&#160;&#160;row.Surname = surname;<br>    &#160;&#160;&#160;&#160;dst.Customer.AddCustomerRow(row);<br>    &#160;&#160;&#160;&#160;try<br>    &#160;&#160;&#160;&#160;&#123;<br>        &#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;slqcon.Open();<br>        &#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;sqladp.Update(dst);<br>    &#160;&#160;&#160;&#160;&#125;<br>    &#160;&#160;&#160;&#160;finally<br>    &#160;&#160;&#160;&#160;&#123;  <br>        &#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;sqlcon.Close();<br>    &#160;&#160;&#160;&#160;&#125;<br>&#125;</pre>
        </dt>
        <dd>&#160;&#160;&#160;&#160;&#160; Figure&#58; Inserting rows using DataAdapter with SQL INSERT statement, then use DataApdater.Update </dd>
    </dl>
    <p>In this example, the SQL is mixed up with the .NET code, and has to be manually updated if the database schema is changed. However, the strongly typed DataSet automatically updates when the database schema changes. </p>
    </li>
    <li>
    <p>Use DataAdapter with a stored procedure for INSERT, then use DataAdapter.Update (strongly-typed-dataset)</p>
    <dl class="goodCode">
        <dt style="width&#58;92.93%;height&#58;639px;">
        <pre>public void DASPInsert(string firstName, string surname)<br>&#123;<br>    &#160;&#160;&#160;&#160;SqlConnection sqlcon = new SqlConnection();<br>    &#160;&#160;&#160;&#160;sqlcon.ConnectionString = &quot;Persist Security Info=False;<br>                  Integrated Security=SSPI; database=northwind;<br>                  server=mySQLServer;Connect Timeout=30&quot;;<br>    &#160;&#160;&#160;&#160;SqlCommand sqlcmd = new SqlCommand();<br>    &#160;&#160;&#160;&#160;sqlcmd.CommandText = &quot;proc_InsertCustomer&quot;;<br>    &#160;&#160;&#160;&#160;sqlcmd.CommandType = CommandType.StoredProcedure;<br>    &#160;&#160;&#160;&#160;sqlcmd.Connection = sqlcon;<br>    &#160;&#160;&#160;&#160;SqlDataAdapter sqladp = new SqlDataAdapter();<br>    &#160;&#160;&#160;&#160;sqladp.InsertCommand = sqlcmd;<br>    &#160;&#160;&#160;&#160;NorthWindCustomer dst = new NorthWindCustomer();<br>    &#160;&#160;&#160;&#160;NorthWindCustomer.CustomerRow row = dst.Customer.NewCustomerRow();<br>    &#160;&#160;&#160;&#160;row.FirstName = firstName;<br>    &#160;&#160;&#160;&#160;row.Surname = surname;<br>    &#160;&#160;&#160;&#160;dst.Customer.AddCustomerRow(row);<br>    <br>    &#160;&#160;&#160;&#160;try<br>    &#160;&#160;&#160;&#160;&#123;<br>        &#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;sqlcon.Open();<br>        &#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;sqladp.Update(dst);<br>    &#160;&#160;&#160;&#160;&#125;<br>    &#160;&#160;&#160;&#160;catch<br>    &#160;&#160;&#160;&#160;&#123;<br>        &#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;MessageBox.Show(<br>            &#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&quot;Unable to open connection.&quot;,<br>            &#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&quot;Error&quot;, MessageBoxButtons.OK, MessageBoxIcon.Error);<br>    &#160;&#160;&#160;&#160;&#125;<br>    &#160;&#160;&#160;&#160;finally<br>    &#160;&#160;&#160;&#160;&#123;<br>        &#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;sqlcon.Close();<br>    &#160;&#160;&#160;&#160;&#125;<br>&#125;</pre>
        </dt>
        <dd>&#160;&#160;&#160;&#160;&#160;Figure&#58; Inserting rows using DataAdapter with a stored procedure for INSERT, then use DataAdapter.Update (strongly-typed-dataset) - best for SQL Server </dd>
    </dl>
    <p>This is the best approach for Microsoft SQL Server. The parameters for the stored procedure are automatically generated and the strongly typed dataset updates when the database schema changes. </p>
    </li>
    <li>
    <p>Use DataAdapter with SQL SELECT statement, then use command builder to automatically create INSERT, UPDATE and DELETE statements as required. Then use DataAdapter.Update (strongly-typed-dataset). </p>
    <dl class="goodCode">
        <dt style="width&#58;93.41%;height&#58;656px;">
        <pre>public void DACmdb(string firstName, string surname)<br>&#123;<br>    &#160;&#160;&#160;&#160;SqlConnection sqlcon = new SqlConnection();<br>    &#160;&#160;&#160;&#160;sqlcon.ConnectionString = &quot;Persist Security Info=False;<br>                  Integrated Security=SSPI; database=northwind;<br>                  server=mySQLServer;Connect Timeout=30&quot;;<br>    &#160;&#160;&#160;&#160;SqlCommand sqlcmd = new SqlCommand();<br>    &#160;&#160;&#160;&#160;sqlcmd.CommandText = &quot;SELECT firstName, surname FROM Customers&quot;;<br>    &#160;&#160;&#160;&#160;sqlcmd.Connection = sqlcon;<br>    &#160;&#160;&#160;&#160;SqlDataAdapter sqladp = new SqlDataAdapter();<br>    &#160;&#160;&#160;&#160;sqladp.SelectCommand = sqlcmd;<br>    &#160;&#160;&#160;&#160;SqlCommandBuilder cmdb = new SqlCommandBuilder(adp);<br>    <br>    &#160;&#160;&#160;&#160;NorthWindCustomer dst = new NorthWindCustomer();<br>    &#160;&#160;&#160;&#160;NorthWindCustomer.CustomerRow row = dst.Customer.NewCustomerRow();<br>    &#160;&#160;&#160;&#160;row.FirstName = firstName;<br>    &#160;&#160;&#160;&#160;row.Surname = surname;<br>    &#160;&#160;&#160;&#160;dst.Customer.AddCustomerRow(row);<br>    <br>    &#160;&#160;&#160;&#160;try<br>    &#160;&#160;&#160;&#160;&#123;<br>        &#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;sqlcon.Open();<br>        &#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;sqladp.Update(dst);<br>    &#160;&#160;&#160;&#160;&#125;<br>    &#160;&#160;&#160;&#160;catch<br>    &#160;&#160;&#160;&#160;&#123;<br>        &#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;MessageBox.Show(<br>            &#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&quot;Unable to open connection.&quot;,<br>            &#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&quot;Error&quot;, MessageBoxButtons.OK, MessageBoxIcon.Error);<br>    &#160;&#160;&#160;&#160;&#125;<br>    &#160;&#160;&#160;&#160;finally<br>    &#160;&#160;&#160;&#160;&#123;<br>        &#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;sqlcon.Close();<br>    &#160;&#160;&#160;&#160;&#125;<br>&#125;</pre>
        </dt>
        <dd>&#160;&#160;&#160;&#160; Figure&#58; Inserting rows using DataAdapter with SQL SELECT statement, then use command builder to automatically create INSERT, UPDATE and DELETE - best for SQL Server</dd>
    </dl>
    <p>&#160;&#160;&#160;&#160; This approach is the best approach for Jet (Access) databases, as stored procedures in Access are difficult to implement and unreliable. The INSERT statement is automatically generated by .NET and the strongly typed databases update when the database schema is changed.</p>
    </li>
</ol>



