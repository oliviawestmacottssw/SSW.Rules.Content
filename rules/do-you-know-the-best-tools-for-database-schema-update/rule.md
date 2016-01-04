---
type: rule
title: Do you know the best tools for Database Schema Update?
uri: do-you-know-the-best-tools-for-database-schema-update
created: 2009-10-06T23:23:45.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 40
  title: Igor Goldobin
- id: 24
  title: Adam Stephensen
- id: 53
  title: Thiago Passos
- id: 34
  title: Brendan Richards

---

 
​It is important when deploying your database for the database to be updated automatically.

There are a number of tools that can be used to update the database as the application can be updated.




- Red Gate SQL Compare + Red Gate SQL Packager (post development model)
- Visual Studio 2013​ Data Dude + Deploy (post development model)
- SQL Management Studio + OSQL  (Free and roll your own)​

​Figure: Bad options for updating database schema​ - No ability to validate that the database hasn't been tampered with​




![](http&#58;//sqldeploy.com/images/SQLDeploy_logo.png)
​Figure: Good option for existing databases - ​SQL Management Studio + SSW SQL Deploy (As you go model)​



[TODO: Logo Required for SQL Validate]


​Figure: Good option for when using EF Code First: SSW SQL Validate



