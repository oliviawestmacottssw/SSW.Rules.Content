---
type: rule
title: Do you remove VBA function names in queries before upsizing queries (Upsizing problem)?
uri: do-you-remove-vba-function-names-in-queries-before-upsizing-queries-upsizing-problem
created: 2010-07-23T03:36:59.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

 This field should not be null (Remove me when you edit this field). 
- Queries referencing value in control, for example Forms![FormName]![ControlName] (Access 2000)
- Select queries that take parameters (Access 2000)
- Select queries where parameter used more than once (All versions of Access)
- Select queries referencing Format function (All versions of Access)


You have to manually edit SQL definition in Microsoft Access (remove or replace keyword) and modify view/stored procedure/function T-SQL in SQL Server after upsizing.


```
SELECT Orders.OrderID,
    "Order Subtotals".Subtotal, 
    FORMAT(ShippedDate,'yyyy') AS Year 
FROM Orders 
INNER JOIN "Order Subtotals" 
    ON (Orders.OrderID="Order Subtotals".OrderID);
```

Figure: Bad example of Access query with FORMAT keyword

```
SELECT Orders.OrderID,
    "Order Subtotals".Subtotal, 
    YEAR(ShippedDate) AS [Year] 
FROM Orders 
INNER JOIN "Order Subtotals" 
    ON (Orders.OrderID="Order Subtotals".OrderID)
```

Figure: Good example of SQL Server view with YEAR keyword 
[Upsizing PRO](http&#58;//www.ssw.com.au/ssw/UpsizingPRO) will check this rule

