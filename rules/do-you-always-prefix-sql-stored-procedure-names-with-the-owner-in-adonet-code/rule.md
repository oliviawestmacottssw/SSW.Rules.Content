---
type: rule
archivedreason: 
title: Do you always prefix SQL stored procedure names with the owner in ADO.NET code?
guid: 059f81e9-77a4-4eb2-8bd0-52fc3e3be0a6
uri: do-you-always-prefix-sql-stored-procedure-names-with-the-owner-in-adonet-code
created: 2009-05-13T06:49:36.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 17
  title: Ryan Tee
related: []
redirects: []

---

Stored procedure names in code should always be prefixed with the owner (usually dbo). This is because if the owner is not specified, SQL Server will look for a procedure with that name for the currently logged on user first, creating a performance hit.   
<!--endintro-->


```
SqlCommand sqlcmd = new SqlCommand(); sqlcmd.CommandText = "<span style="background-color:rgb(255, 0, 0);">
                    proc_InsertCustomer</span>" sqlcmd.CommandType
                    = CommandType.StoredProcedure; sqlcmd.Connection = sqlcon;
```

Bad Example 

```
SqlCommand sqlcmd = new SqlCommand(); sqlcmd.CommandText = "
                     <span style="background-color:rgb(0, 255, 0);">dbo.proc_InsertCustomer</span>"; sqlcmd.CommandType
                     = CommandType.StoredProcedure; sqlcmd.Connection = sqlcon;
```

Good Example 

| We have a program called [SSW Code Auditor](http&#58;//www.ssw.com.au/ssw/CodeAuditor/Default.aspx) to check for this rule. |
| --- |
