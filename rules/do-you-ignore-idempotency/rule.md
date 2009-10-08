---
type: rule
title: Do you ignore Idempotency?
uri: do-you-ignore-idempotency
created: 2009-10-05T06:03:28.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

 This field should not be null (Remove me when you edit this field). 
Database scripts should be run in order (into separate sequential files), as per the rule [Do you script out all changes?](http&#58;//www.ssw.com.au/ssw/standards/rules/rulestobettersqlserverdatabases.aspx#ScriptOutChanges)

 Therefore developers should not worry about idempotency, as the script will run in the order it was created. Actually, if they are doing this, then **\*they want to see the errors\***. It means that the database is not in the state that they expect.


```
IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES 
           WHERE TABLE_TYPE='BASE TABLE' AND  TABLE_NAME='Employees') 
    ALTER TABLE [dbo].[Employees]( …… ) ON [PRIMARY] 
ELSE 
    CREATE TABLE [dbo].[Employees]( …… ) ON [PRIMARY]
```

Bad example – worrying about the idempotency should not be done, if you plan to run your scripts in the order they were created 

```
CREATE TABLE [dbo].[Employees](
    ……
) ON [PRIMARY]
```

Good example – not worrying about the idempotency. If errors occur we don’t want them to be hidden + it is easier to read See the concept of [Idempotence on WikiPedia](http&#58;//en.wikipedia.org/wiki/Idempotence)
