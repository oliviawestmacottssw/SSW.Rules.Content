---
type: rule
title: Do you know you can't think of data the same way?
uri: do-you-know-you-cant-think-of-data-the-same-way
created: 2009-05-21T23:35:36.0000000Z
authors:
- id: 18
  title: Jay Lin

---

In SQL Server you have tables to store data.  Then you have Views, Relations and Stored Procedures.

SharePoint gives us Lists where we can store rows and columns of data, but it is not the same as a full database.
<br> <br>
- There are no joints out of SharePoint – you can do limited operations with lookup fields but they are not the same as joints in SQL Server
- Views in SharePoint are filters, grouping and sort on a single list only.
- Formula fields in SharePoint are only updated when the row is changed.  If you change the lookup value in the lookup list, it will not change any of the items using formula fields that are currently referencing that lookup.
- No stored procedures in SharePoint


Database remains the best at doing database work.  SharePoint is OK at creating quick lists and working with simple lists, but it is not a database server.
