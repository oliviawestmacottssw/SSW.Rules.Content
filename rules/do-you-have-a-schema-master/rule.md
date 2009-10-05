---
type: rule
title: Do you have a "Schema Master"?
uri: do-you-have-a-schema-master
created: 2009-10-05T05:51:48.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

 This field should not be null (Remove me when you edit this field). 
If your project has a database, you need to select a ‘Schema Master’. This is the one person who is allowed to make modifications to the database. These include:

- Creating, Modifying and Deleting tables and columns
- Relationships
- Modify lookup data (see our [Do you deploy lookup data?](/Standards/CodeAndApplicationDesign/RulesToBetterSQLServerSchemaDeployment/Pages/DoYouDeployLookupData.aspx))

![](/Standards/CodeAndApplicationDesign/RulesToBetterSQLServerSchemaDeployment/PublishingImages/SQLScriptInTFS.png) Figure: The Applications Database stores version info in a table called \_zsVersion 
