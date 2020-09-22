---
type: rule
title: Do you run Test-SPContentDatabase before migration
uri: do-you-run-test-spcontentdatabase-before-migration
created: 2016-05-19T08:05:06.0000000Z
authors:
- id: 9
  title: William Yin

---

 
**​​​Assumption:**

1. You have already installed th​e customized wsp package you know.
2. You have restored the content database to SQL server
3. You haven't attach the content database yet.


It is strongly recommend to run a pre-migration check on the content database before attaching it to trigger the migration process.
 
**Steps:**

1. ​Run SharePoint PowerShell Console as admini​strator
2. ​Run the command below​​​​
​​​​**Test-SPContentDatabase** **-****name **WSS\_Content\_DB **-****webapplication **http://sitename​
3. Check the output log, ensure there isn't any errors.


