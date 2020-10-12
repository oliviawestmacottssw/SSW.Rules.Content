---
type: rule
title: General - Do you use a SQL Server Indexes Naming Standard?
uri: general---do-you-use-a-sql-server-indexes-naming-standard
created: 2019-12-31T04:47:26.0000000Z
authors: []

---

This standard outlines the procedure on naming Indexes at SSW for SQL Server. Use this standard when creating new Indexes or if you find an older Index that doesn't follow that standard.



 
**Note:** There is not a lot of use naming Indexes - we only do it when we are printing out documentation or using the 'Index Tuning Wizard' - then it becomes really handy.
Do you agree with them all? Are we missing some? Let us know what you think.

Index names are to have this syntax:
[pkc\_] [TableName] by [FieldName]
[   1  ] [    2        ]      [    3       ]
[1] All indexes must have a corresponding prefix.


| **Prefix** <br> |  **Type** <br> |
| --- | --- |
| pkc\_<br> | Primary Key, Clustered<br> |
| pknc\_<br> | Primary Key, Non Clustered<br> |
| ncu\_<br> | Non Clustered, Unique<br> |
| cu\_<br> | Clustered, Unique<br> |
| nc\_<br> | Non Clustered (Most Common)<br> |
| <br> | <br> |


Make unique index name if possible. Ie. ProductName
[2] The name of the table that the Index refers to.
[3] The name of the column(s) that the Index refers to.

[[greyBox | Bad Example]]
|  Index 'BillingID'
| Primary Key 'aaaaaClient\_PK'
|

[[greyBox | Good Example]]
|  'nc\_ClientDiary\_BillingID'
| 'pknc\_ClientDiary\_ClientID'
|
