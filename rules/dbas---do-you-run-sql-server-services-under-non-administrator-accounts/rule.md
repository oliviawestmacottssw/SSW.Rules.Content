---
type: rule
title: ​DBAs - Do you run SQL Server Services under non-Administrator accounts?
uri: dbas---do-you-run-sql-server-services-under-non-administrator-accounts
created: 2019-11-18T23:40:32.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

You should always run all SQL Server services with the lowest possible privileges allowed in case the account is compromised. SQL Server setup makes the whole process of granting privileges a whole lot easier because it automatically creates groups with all the necessary permissions for you!
 
![ SQL Server now creates groups for all the SQL Server services with the bare minimum permissions for you](SQLDatabases_RunAsAccount_GroupsCreated.png)

If you are running any SQL Server Service in a user account that has administrator privileges a user that compromises the account could do anything that administrator could do - including playing around with the registry with procedures like xp\_regdeletevalue. So, if you use an Administrator account, you're in effect giving away the keys to the house. Is this something you want to do?
