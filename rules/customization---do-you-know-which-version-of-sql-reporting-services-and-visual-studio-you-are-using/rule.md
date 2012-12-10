---
type: rule
title: Customization - Do you know which version of SQL Reporting Services and Visual Studio you are using?
uri: customization---do-you-know-which-version-of-sql-reporting-services-and-visual-studio-you-are-using
created: 2012-12-10T18:37:44.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 32
  title: Mehmet Ozdemir

---


CRM 3.0 is in .NET 1.1 so it was designed to work with:

- SQL Server 2000 (even better to use 2005)
- Reporting Services 2000 (design reports in VS.NET 2003)
- Callouts in VS.NET 2003

 
**Tip #1:** Do try to use SQL 2005 if available - it is marginally faster.

**Tip #2:** Don't try working in VS.NET 2005 - there are workarounds but they become           very, very painful.

**Tip #3:** SQL Reporting Services and the .rdl files are not backward compatible -           there is no hope of doing them in 2005 and back porting the RDL.

