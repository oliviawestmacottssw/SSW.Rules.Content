---
type: rule
title: Do you avoid using duplicate connection string in web.config?
uri: do-you-avoid-using-duplicate-connection-string-in-webconfig
created: 2009-05-11T06:55:57.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 17
  title: Ryan Tee

---

Since we have many ways to use Connection String in .NET 2.0, it is probably that we are using duplicate connection string in web.config. <br> 

```
<connectionStrings>   <add name="ConnectionString" connectionString="Server=(local);Database=NorthWind;" /></connectionStrings><appSettings>   <add key="ConnectionString" value="Server=(local);Database=NorthWind;"/></appSettings>
```

Bad example - use duplicate connection string in web.config. 

| We have a program called [SSW Code Auditor](http&#58;//www.ssw.com.au/ssw/CodeAuditor/) to check for this rule. |
| --- |
