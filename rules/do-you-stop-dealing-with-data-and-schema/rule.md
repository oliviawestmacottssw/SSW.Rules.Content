---
type: rule
title: Do you stop dealing with Data and Schema?
uri: do-you-stop-dealing-with-data-and-schema
created: 2009-03-10T06:36:56.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

 This field should not be null (Remove me when you edit this field). 
Take a version control approach. It doesn't have to be too complicated, but you should keep a history of structure changes in a table. Some developers [use a text file (.sql)](http&#58;//www.ssw.com.au/ssw/Standards/Rules/RulesToBetterSQLServerDatabases.aspx#General) or hardcode it in code, that's fine, just don't make changes in the interface (i.e.. Access or Enterprise Manager). Changes should be made programmatically, or in a method that they can be played back.

An assumption to this is you have a front-end and backend table that is used to record the version number.
![Table with cross through it](/Standards/Management/RulesToSuccessfulProjects/PublishingImages/imgTableWithCrossThroughIt.gif) Figure: Never make a change manually in Enterprise Manager or Access ![ ](/Standards/Management/RulesToSuccessfulProjects/PublishingImages/SaveChangeScript.gif) Figure: Always save your changes in script ![ ](/Standards/Management/RulesToSuccessfulProjects/PublishingImages/ChangeScripts.gif) Figure: Name them in the order they're executed ![ ](/Standards/Management/RulesToSuccessfulProjects/PublishingImages/SampleTable.gif) Figure: An example of a backend table recording the version numbers 
**Tip:** If you’re using Next Gen and you’re changing just one table, then just regenerate for that table


| We have a program called [SSW SQL Deploy](http&#58;//www.ssw.com.au/ssw/SQLDeploy/Default.aspx) to solve this problem and automatically make schema changes. |
| --- |


