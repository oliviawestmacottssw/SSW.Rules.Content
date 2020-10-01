---
type: rule
title: Do you use the AllowZeroLength property on a field (Upsizing Problem)?
uri: do-you-use-the-allowzerolength-property-on-a-field-upsizing-problem
created: 2010-07-23T02:36:10.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

- The value that you select for the AllowZeroLength property determines whether zero length strings ("") may be inserted into a field. Currently, the Upsizing Wizard does not create a constraint or trigger against an upsized table to enforce this rule. Instead, you must manually create a Check Constraint on the columns once the upsizing process is complete.
- Still an issue in Access 2000 -2003

[Upsizing PRO](http&#58;//www.ssw.com.au/ssw/UpsizingPRO) will check this rule
