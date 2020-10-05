---
type: rule
title: Do you add the Application Name in the SQL Server connection string?
uri: do-you-add-the-application-name-in-the-sql-server-connection-string
created: 2018-04-26T21:01:36.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

You should always add the application name to the connection string so that SQL Server will know which application is connecting, and which database is used by that application. This will also allow SQL Profiler to trace individual application which helps you monitor performance or resolve conflicts.

 
​&lt;add key="Connection" value="Integrated Security=SSPI;Persist Security Info=False;Initial Catalog=Biotrack01;Data Source=sheep;"/&gt;
Bad example - The connection string without Application Name

&lt;add key="Connection" value="Integrated Security=SSPI;Persist Security 
 Info=False;Initial Catalog=Biotrack01;Data Source=sheep; 
 Application Name=Biotracker"/&gt; // Good Code - Application Name is added in the connection string.​
​​Good example - The connection string with Application Name​
