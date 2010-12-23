---
type: rule
title: Do you lock the SharePoint Content Database before making a backup?
uri: do-you-lock-the-sharepoint-content-database-before-making-a-backup
created: 2010-12-23T06:55:11.0000000Z
authors:
- id: 36
  title: Daniel Šmon
- id: 9
  title: William Yin
- id: 21
  title: Matthew Hodgkins

---


Even though you have advised staff members a migration is taking place – you can guarantee someone will try to check-in or edit documents. The best way to prevent this is to put your content database into read only mode.

1.    On your database server open **SQL Server Management Studio**

2.    Right click on the content database associated with the site collection your migrating | **Properties**

3.    Choose **Options **| Scroll to the bottom of the options list

4.    For the **Database Read-Only** choose **True![](/ITAndNetworking/SharePointMigration/PublishingImages/LocLSQLDB.jpg)****
**

Figure - Database Properties | Options | Database-Read Only

5.    Now it’s safe to take a backup of your content database

**NOTE: ** When some SharePoint timer services are run it may cause the site to display errors when the database is in read only mode
  Even though you have advised staff members a migration is taking place – you can guarantee someone will try to check-in or edit documents. The best way to prevent this is to put your content database into read only mode.    
