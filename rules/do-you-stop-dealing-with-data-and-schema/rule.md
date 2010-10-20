---
type: rule
title: Do you stop dealing with Data and Schema?
uri: do-you-stop-dealing-with-data-and-schema
created: 2009-03-10T06:36:56.0000000Z
authors:
- id: 1
  title: Adam Cogan

---


Why don't most developers plan ahead? Take an average VB or Access application that you sell to a few customers. When the customer wants a new version, there is no problem giving the customer the new mdb or exe. But what if you made a back-end structural [changes to your database](http&#58;//www.ssw.com.au/ssw/Standards/Rules/DataSchemaStandard.aspx)? Big hassle! You need to compare the database to remind you what was changed. Sure there are utilities for this - for Access backends you can use [SSW Data Renovator](http&#58;//www.ssw.com.au/ssw/DataRenovator/Default.aspx) or for SQL Server backends there is [Red-gate SQL Compare](http&#58;//www.ssw.com.au/ssw/Redirect/RedGateSQLDataCompare.htm)![leave site](http&#58;//www.ssw.com.au/ssw/Images/LeaveSite.gif) - but why go to this trouble?

Take a version control approach. It doesn't have to be too complicated, but you should keep a history of structure changes in a table. Some developers [use a text file (.sql)](http&#58;//www.ssw.com.au/ssw/Standards/Rules/RulesToBetterSQLServerDatabases.aspx#General) or hardcode it in code, that's fine, just don't make changes in the interface (i.e.. Access or Enterprise Manager). Changes should be made programmatically, or in a method that they can be played back.

An assumption to this is you have a front-end and backend table that is used to record the version number.
![Table with cross through it](/Management/RulesToSuccessfulProjects/PublishingImages/imgTableWithCrossThroughIt.gif) Figure: Never make a change manually in Enterprise Manager or Access ![ ](/Management/RulesToSuccessfulProjects/PublishingImages/SaveChangeScript.gif) Figure: Always save your changes in script ![ ](/Management/RulesToSuccessfulProjects/PublishingImages/ChangeScripts.gif) Figure: Name them in the order they're executed ![ ](/Management/RulesToSuccessfulProjects/PublishingImages/SampleTable.gif) Figure: An example of a backend table recording the version numbers 
**Tip:** If you’re using Next Gen and you’re changing just one table, then just regenerate for that table


| We have a program called [SSW SQL Deploy](http&#58;//www.ssw.com.au/ssw/SQLDeploy/Default.aspx) to solve this problem and automatically make schema changes. |
| --- |


