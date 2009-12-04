---
type: rule
title: Do you hard code your ConnectionString?
uri: do-you-hard-code-your-connectionstring
created: 2009-04-29T05:36:44.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 17
  title: Ryan Tee

---

 This field should not be null (Remove me when you edit this field). 

```
connection.ConnectionString = "
Provider=SQLOLEDB;
Data Source=server_name_or_address; Initial Catalog=database_name;
User ID=username; Password=password; ";

   connection.Open();
```

Bad code - use the lengthy connection string.

```
connection.ConnectionString = ConfigurationManager.Items["ConnectionString"];

 connection.Open();
```

Figure: Good Code - Use ConfigurationManager to handle the connection string.

| We have a program called [SSW Code Auditor](http&#58;//www.ssw.com.au/ssw/CodeAuditor/Default.aspx) to check for this rule.  |
| --- |


