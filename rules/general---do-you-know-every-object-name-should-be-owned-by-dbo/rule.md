---
type: rule
title: General - Do you know every object name should be owned by dbo?
uri: general---do-you-know-every-object-name-should-be-owned-by-dbo
created: 2019-11-14T21:51:26.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

 
​​​The reason is that you avoid ownership chain problems. Where Mary owns an object, Fred can read the object and then he creates a proc and he gives permission to Tom to execute. But Tom cannot because there is a product chain of ownership.​​​​
 
CREATE PROCEDURE [Adam Cogan].[Sales by Year]

@Beginning\_Date DateTime,

@Ending\_Date DateTime AS

SELECT Orders.ShippedDate

,Orders.OrderID

,"vwOrderSubTotals".Subtotal

,DATENAME(yy,ShippedDate) AS Year

FROM Orders

INNER JOIN "vwOrderSubTotals"

ON Orders.OrderID = "vwOrderSubTotals".OrderID

WHERE Orders.ShippedDate Between @Beginning\_Date And @Ending\_Date
Figure: Bad Example​

CREATE PROCEDURE [dbo].[Sales by Year]

 @Beginning\_Date DateTime,

 @Ending\_Date DateTime AS

 SELECT Orders.ShippedDate

 ,Orders.OrderID

 ,"vwOrderSubTotals".Subtotal

 ,DATENAME(yy,ShippedDate) AS Year

 FROM Orders

 INNER JOIN "vwOrderSubTotals"

 ON Orders.OrderID = "vwOrderSubTotals".OrderID

 WHERE Orders.ShippedDate Between @Beginning\_Date And @Ending\_Date
Figure: Good E​​​xample​​​



