---
type: rule
title: Do you follow naming conventions for your Boolean Property?
uri: do-you-follow-naming-conventions-for-your-boolean-property
created: 2018-04-25T21:35:27.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

Boolean Properties must be prefixed by a verb. Verbs like "Supports", "Allow", "Accept", "Use" should be valid. Also properties like "Visible", "Available" should be accepted (maybe not). [Here is how we name Boolean columns in SQL databases.](https&#58;//www.ssw.com.au/ssw/Standards/Rules/RulestoBetterSQLServerdatabases.aspx#BitFields)

 
public bool Enable { get; set; }
public bool Invoice { get; set; }
Bad Example 

public bool Enabled { get; set; }
public bool IsInvoiceSent { get; set; }
Good Example - Naming Convention for Boolean Property

We have a program called [SSW Code Auditor](https&#58;//www.ssw.com.au/ssw/CodeAuditor/) to check for this rule.​
