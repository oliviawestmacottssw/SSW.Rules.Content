---
type: rule
title: Stored Procedures - Do you use transactions for complicated stored procedures?
uri: stored-procedures---do-you-use-transactions-for-complicated-stored-procedures
created: 2019-11-12T23:23:19.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

 
​A transaction means an atomic operation, it assures that all operations within the transaction are successful, if not, the transaction will cancel all operations and roll back to the original state of the database, that means no dirty data and mess exists in the database, so if a stored procedure has many steps, and each step has relation with other steps, it is strongly recommended that you encapsulate the procedure in a transaction.​
 
ALTER PROCEDURE [dbo].[procInit]
AS
 DELETE ParaLeft
 DELETE ParaRight
 INSERT INTO ParaLeft (ParaID)
 SELECT ParaID FROM Para
Figure: Bad Example - No tran​saction here, if any of operations fail, the database will only partially update, resulting in an unwanted result.

ALTER PROCEDURE [dbo].[procInit]
AS
 BEGIN TRANSACTION
 DELETE ParaLeft
 DELETE ParaRight
 INSERT INTO ParaLeft (ParaID)
 SELECT ParaID FROM Para
 COMMIT
Figure: Good Example - Using a transaction to assure that all operations within the transaction will be successful, otherwise, the database will roll back to the original state​.

