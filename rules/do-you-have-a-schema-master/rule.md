---
type: rule
title: Do you have a "Schema Master"?
uri: do-you-have-a-schema-master
created: 2009-10-05T05:51:48.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

You have a web site master right? This is the central point of contact if the site goes down.
<br>When developing an application, all members can code. However schema changes being done by many developers often can lead to trouble. 

<br>Who is "Schema Master"? What does he do? <br> 
![ One person should be the 'Schema Master', on an average sized project ](Nick.png) 
(of 5-10 devs) 
If your project has a database, you need to select a "Schema Master". This is the one person who should review all modifications to the database. These include:

- Creating, Modifying and Deleting tables and columns
- Relationships
- Modify [Controlled Lookup Data](/Pages/DoYouDeployLookupData.aspx)

 The "Schema Master" in a development shop is often the lead programmer on the team. They are in charge of all database changes and scripts. Team members should still feel free to make changes, just get them double checked by the Schema Master.
![ The Applications Database stores version info in a table called \_zsVersion ](zsVersionTable.png) 

![ Only a "Schema Master" checks in the .sql files ](SQLScriptInTFS.png)
