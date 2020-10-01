---
type: rule
title: Do you avoid parameter queries with EXISTS keyword and comparison operators (<> or =)(Upsizing Problem)?
uri: do-you-avoid-parameter-queries-with-exists-keyword-and-comparison-operators--or-upsizing-problem
created: 2010-07-23T03:28:36.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

The MS Upsizing Wizard cannot upsize Microsoft Access queries containing

- EXISTS &lt;&gt; FALSE/TRUE or
- EXISTS = FALSE/TRUE


For example, the following query will not be upsized:


```
PARAMETERS [@Employee Last Name] Text ( 20 );    
SELECT Orders.OrderID
, Orders.CustomerID
, Orders.EmployeeID
FROM Orders
WHERE EXISTS (SELECT EmployeeID
 FROM Employees 
 WHERE LastName= [@Employee Last Name] 
 AND Employees.EmployeeID=Orders.EmployeeID) <> FALSE
```

Figure: Bad example of Access query with EXISTS keyword and comparison operator 

```
PARAMETERS [@Employee Last Name] Text ( 20 ); 
SELECT Orders.OrderID
, Orders.CustomerID
, Orders.EmployeeID
FROM Orders
WHERE EXISTS (SELECT EmployeeID 
 FROM Employees
 WHERE LastName= [@Employee Last Name] 
 AND Employees.EmployeeID=Orders.EmployeeID)
```

Figure: Good example of Access query with EXISTS keyword and without comparison operatorIn order to get the good example syntax you must switch from Design View window to SQL View in query designer window and save query definition.
