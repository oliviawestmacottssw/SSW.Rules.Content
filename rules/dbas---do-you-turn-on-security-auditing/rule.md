---
type: rule
title: DBAs - Do you turn on security auditing?
uri: dbas---do-you-turn-on-security-auditing
created: 2019-11-21T17:55:00.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

 
​​Configure login security auditing:​

- Not on by default
- Configure on the security tab of Server Properties in SQL Server Management Studio
- Enable for Failure
- View using the Windows Event Viewer​

 ​![SQLDatabases_EnableAuditing.png](TurnOnSqlSecurityAuditing.png)Figure: Enable Auditing for SQL Server logins**Note:** You can turn on a trace for SQL DDL operations statements.​
