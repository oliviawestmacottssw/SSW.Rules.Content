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

 
It is important when deploying your database for the database to be updated automatically.​​​

There are a number of tools that can be used to update the database as the application can be updated.

- [Entity Framework Core Migrations](https&#58;//docs.microsoft.com/en-us/ef/core/managing-schemas/migrations/) (This is the suggested method if you are starting a new project)
- [DAC Support For SQL Server Objects and Versions](https&#58;//technet.microsoft.com/en-us/library/ee210549%28v=sql.110%29.aspx)  (.dacpac files)
- [DBUp](https&#58;//dbup.readthedocs.io/en/latest/)


Legacy full framework

- [SQL Deploy](http&#58;//sqldeploy.com/)  (This is the suggested tool if you are not using Entity Framework Code First)
- DBUp + SQL verify


Bad options for updating database schema - No ability to validate that the database hasn't been tampered with

- SQL Management Studio + OSQL  (Free and roll your own)
- Visual Studio 2017 + [SQL Server Data Tools](https&#58;//visualstudio.microsoft.com/vs/features/ssdt/) (Formerly Data Dude) + Deploy (post-development model)
- Red Gate SQL Compare + Red Gate SQL Packager (post-development model)


