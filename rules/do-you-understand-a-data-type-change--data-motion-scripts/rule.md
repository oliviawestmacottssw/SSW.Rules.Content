---
type: rule
title: Do you understand a data type change = "Data Motion Scripts"?
uri: do-you-understand-a-data-type-change--data-motion-scripts
created: 2009-10-07T00:12:39.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 14
  title: Martin Hinshelwood
- id: 44
  title: Duncan Hunter
- id: 34
  title: Brendan Richards
- id: 53
  title: Thiago Passos

---

 Scripting out a schema change is easy, worrying about data is not. "'Data motion" refers to a change in the meaning of data, which will require scripts which touch data and schema. 

<br>Let's look at an example: <br> 
We have a 'Gender' column (that is a Boolean) storing 0's and 1's. All works well for a while.
![](/Standards/SoftwareDevelopment/RulesToBetterSQLServerSchemaDeployment/PublishingImages/TableBit.jpg) Figure: Anything wrong this Gender column?   Later you learn you need to change the data type to char(2) to support 'M', 'F', 'T', 'NA' and 'U' ![](/Standards/SoftwareDevelopment/RulesToBetterSQLServerSchemaDeployment/PublishingImages/CasterSemenya.jpg) Figure: Caster Semenya has taught us a thing or two about the right data type for Gender  The data then must be migrated to the new data type this way: 
1. Rename 'Gender' to 'ztGender' \*
2. Add a new column 'Gender' with type char(2)
3. Insert the existing data from 'ztGender' to 'Gender' (map 0 to 'F' and 1 to 'M')
4. Delete the column ztGender\*

 \*Note: zt stands for Temporary ![](/Standards/SoftwareDevelopment/RulesToBetterSQLServerSchemaDeployment/PublishingImages/TableChar.jpg) Figure: Changing the data type and data required a ["Data Motion Script"](/Standards/SoftwareDevelopment/RulesToBetterSQLServerSchemaDeployment/Pages/DoYouHaveAnUnderstandingOfSchemaChangesAndTheirIncreasingComplexity.aspx) 
Data Dude does not support this scenario, which is why we don't recommend it.
![](/Standards/SoftwareDevelopment/RulesToBetterSQLServerSchemaDeployment/PublishingImages/DataDude-BadExample.jpg)
  Bad Example - Don't use Data Dude
