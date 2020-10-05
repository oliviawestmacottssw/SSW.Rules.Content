---
type: rule
title: Do you keep SharePoint databases in a separate SQL instance?
uri: do-you-keep-sharepoint-databases-in-a-separate-sql-instance
created: 2018-06-25T23:34:07.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 9
  title: William Yin

---

Because SharePoint server will create quite a few databases, it’s easier to manage them in a separate SQL instance rather than mixing it with other system’s databases:
 ​​​
![](sharepoint-database-bad.png)Bad example - mixed with other systems' database​​​
![](sharepoint-database-good.png)Good example - SharePoint related databases are in a separate SQL instance from other systems' databases​
