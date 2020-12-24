---
type: rule
archivedreason: 
title: General - Do you use a SQL Server Relationship Naming Standard?
guid: d937d293-104e-4e65-8015-a88738c58045
uri: general-do-you-use-a-sql-server-relationship-naming-standard
created: 2019-12-31T05:04:48.0000000Z
authors:
- id: 1
  title: Adam Cogan
related: []
redirects: []

---

This standard outlines the procedure on naming Relationships at SSW for SQL Server. Use this standard when creating new Relationships or if you find an older Relationship that doesn't follow that standard.

<!--endintro-->

Do you agree with them all? Are we missing some? Let us know what you think.

### Syntax

Relationship names are to have this syntax:
[PrimaryTable] - [ForeignTable]
[        1       ] - [        2       ]

[1] The table whose columns are referenced by other tables in a one-to-one or one-to-many relationship.
Rather than accepting the default value i.e. ClientAccount\_FK01 that is given from upsizing.

![](imgRelationshipPic1.gif)

::: bad
Figure: Bad Example - using the default relationship name

:::


We recommend using Prod-ClientAccount.

![](imgRelationshipPic2.gif)

::: good
Figure: Good Example - using a more descriptive relationship name

:::




The good thing is when you look at the relationship from the other side it is there as well.

![Relationship name shown on the other table](imgRelationshipPic3.gif)
** 
We also believe in using Cascade Updates - but never cascade deletes.
