---
type: rule
title: Stored Procedures - Do you know SQL stored procedure names should be prefixed with the owner?
uri: stored-procedures---do-you-know-sql-stored-procedure-names-should-be-prefixed-with-the-owner
created: 2019-11-12T23:28:52.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

Always specify the schema prefix when creating stored procedures. This way you know that it will always be dbo.procedure\_name no matter who is logged in when it is created.

There are 2 other benefits to including the schema prefix on all object references:

1. This prevents the database engine from checking for an object under the users schema first
2. Also avoids the issue where multiple plans are cached for the exact same statement/batch just because they were executed by users with different default schemas.


 
Aaron Bertrand agrees with this rule - [My stored procedure "best practices" checklist](https&#58;//sqlblog.org/2008/10/30/my-stored-procedure-best-practices-checklist).

CREATE PROCEDURE procCustomer\_Update @CustomerID INT, ….. BEGIN
Figure: Bad example
CREATE PROCEDURE dbo.procCustomer\_Update @CustomerID INT, ….. BEGIN
Figure: Good example
