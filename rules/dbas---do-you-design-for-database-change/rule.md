---
type: rule
title: ​DBAs - Do you design for database change?
uri: dbas---do-you-design-for-database-change
created: 2019-11-18T19:10:50.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

 
​​Many developers are frightened of making a change to the existing database because they just don't know what applications are using it. This is especially a problem when you are dealing with databases that you did not create. Here are some approaches to this issue:
 
1. You could run around the office and find some one and hope they know (unbelievably this seems this the most common method!)
2. Trawl through source control, all network locations and all the source code around to check what connection strings are being used
3. You can have a zsApplication table and manually populate with application it uses (Recommended). This can be populated with a run of a SQL profiler over a period of a week so all usage is captured. <br>      ![SQLDatabases_zsApplication.png](SQLDatabases_zsApplication.png)Figure​: Add a zsApplication table to make applications that use it visible to all developers
4. Keep a constantly running login Audit with a SQL Server Profiler Trace that saves to a table​ and make sure all applications have an application name in their connection string. This method is the most comprehensive option but is not recommended because you get a constant performance hit from SQL Profiler running.
![2020-01-09_18-55-46.png](2020-01-09_18-55-46.png)
Figure: SQL Profiler can help you design for change with auditing of Login events by giving you a guide on what applications are connecting to your database


