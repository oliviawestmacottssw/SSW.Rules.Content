---
type: rule
title: Do you have complex queries (Upsizing Problem)?
uri: do-you-have-complex-queries-upsizing-problem
created: 2010-07-23T03:23:22.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

 This field should not be null (Remove me when you edit this field). 
- Crosstab queries
- Action queries (append, delete, make-table, update) that take parameters
- Action queries that contain nested queries
- SQL pass-through queries
- SQL Data Definition Language (DDL) queries
- Union queries
- Queries that reference values on a form




You must manually re-create queries that the Upsizing Tools do not migrate.

