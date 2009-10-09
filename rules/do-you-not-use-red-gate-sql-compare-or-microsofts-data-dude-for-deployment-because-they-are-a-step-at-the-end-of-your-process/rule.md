---
type: rule
title: Do you *not* use Red-Gate SQL Compare (or Microsoft's Data Dude) for deployment (because they are a step at the end of your process)?
uri: do-you-not-use-red-gate-sql-compare-or-microsofts-data-dude-for-deployment-because-they-are-a-step-at-the-end-of-your-process
created: 2009-10-05T23:21:49.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

 This field should not be null (Remove me when you edit this field). ![](/Standards/SoftwareDevelopment/RulesToBetterSQLServerSchemaDeployment/PublishingImages/SQLCompareSync.png) Figure: You can use SQL Compare to make two databases the same ![](/Standards/SoftwareDevelopment/RulesToBetterSQLServerSchemaDeployment/PublishingImages/SQLCompareTables.png) Figure: SQL Compare clearly shows some tables are missing 
So if you want to compare 2 databases SQL Compare (or Data Dudes Compare) is great tools. They even let you synchronize sweetly between these 2 databases. However, if you are doing this at the end of your release cycle, you have a problem.  Your schema deployment process is broken.

What you should be doing is seeing your [Schema Master](/Standards/SoftwareDevelopment/RulesToBetterSQLServerSchemaDeployment/Pages/DoYouHaveASchemaMaster.aspx "Database Schema Master") each time you have a new .sql file. You do this during the development process, not at the end in the package and deployment process.
![](/Standards/SoftwareDevelopment/RulesToBetterSQLServerSchemaDeployment/PublishingImages/SQLScriptInTFS.png) Figure: Give your SQL scripts to 'Schema Master' who will, check them into TFS, then run them Note: We have a tool called [SQL Deploy](http&#58;//www.ssw.com.au/ssw/SQLDeploy/) to help with automatic deployment.
