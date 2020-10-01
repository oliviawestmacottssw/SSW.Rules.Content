---
type: rule
title: Do you have complex queries (Upsizing Problem)?
uri: do-you-have-complex-queries-upsizing-problem
created: 2010-07-23T03:23:22.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

The Upsizing Tools do not try to upsize every type of Microsoft Access query that you may have in your Access (Jet) database. The following varieties of queries will not upsize: <br> 
- Crosstab queries
- Action queries (append, delete, make-table, update) that take parameters
- Action queries that contain nested queries
- SQL pass-through queries
- SQL Data Definition Language (DDL) queries
- Union queries
- Queries that reference values on a form




You must manually re-create queries that the Upsizing Tools do not migrate.
