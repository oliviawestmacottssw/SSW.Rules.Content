---
type: rule
title: General - Do you know the naming convention for use on database server test and production?
uri: general---do-you-know-the-naming-convention-for-use-on-database-server-test-and-production
created: 2019-11-14T21:59:12.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

 
Generally, every client should have a dev and a test database, so the dev database needs to have the postfix "Dev" and the test database need to have the postfix "Test"(E.g. SSWCRMDev, SSWCRMTest). However, you don't need any postfix for the production database.​​​
 ![BadDBName.gif](BadDBName.gif)​Figure: Bad Example - Database with bad names
![GoodDBName.gif](GoodDBName.gif)Figure: Good Example - ​Database with standard names​

