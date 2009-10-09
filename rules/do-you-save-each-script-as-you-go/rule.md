---
type: rule
title: Do you save each script as you go?
uri: do-you-save-each-script-as-you-go
created: 2009-10-06T23:42:21.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 40
  title: Igor Goldobin

---

 This field should not be null (Remove me when you edit this field). 
1. When you have an error you can see exactly which script introduced it
2. You don't have to use a compare tool like Red-Gate SQL Compare at the end of your development cycle
3. Your application can automatically make schema changes
4. The application can have a "Create" database button when installed for the first time
5. The application can have an "Upgrade" button and work out itself if this new version needs scripts to be run
6. The application can tell if it is an old version (as a newer version may have upgraded the schema), so you only use the latest clients
7. The application can have a "Reconcile" feature that compares the current schema to what it should be


![](/Standards/SoftwareDevelopment/RulesToBetterSQLServerSchemaDeployment/PublishingImages/ChangeScripts.jpg) Figure: A list of change SQL scripts, each file name is in the correct format 
**Is there a file naming convention to follow?**
 The script file naming convention should be XXXXX\_ObjectType\_ObjectName\_ColumnName\_Description\_SchemaMasterInitials.sql 

 eg.  00089\_Table\_Employee\_Gender\_ChangeFromBitToChar\_AC.sql

