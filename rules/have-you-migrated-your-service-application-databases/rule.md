---
type: rule
title: Have you migrated your service application databases
uri: have-you-migrated-your-service-application-databases
created: 2013-04-26T00:12:43.0000000Z
authors:
- id: 28
  title: Daragh Bannigan
- id: 9
  title: William Yin

---

 Depends on your SharePoint farm, you can upgrade the service applications database to SharePoint 2013.

 
​In our case, we have upgraded the below several service application databases:

- Secure Store
- User Profiles
- Managed Metadata
- Business Connectivity Services


Steps:

1. Backup databases of SharePoint 2010 Service Application.

2. Restore and attach databases to SharePoint 2013 SQL server.

3. Create service application in SharePoint 2013 Central Admin site with the restored database.

4. Test.

5. Done.

