---
type: rule
title: Do you have a general Contact Detail table?
uri: do-you-have-a-general-contact-detail-table
created: 2019-11-22T21:41:18.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

 
It is common to have a Contact Detail table to store your contact information such as phone numbers. Below is an example of a Contact Detail table and its related tables. This is bad because the PartyPhone table is too specific for a phone number and you have to add a new table to save an email or other contact information if this is needed in the future.​
 ​![ContactDetailTable_bad.png](ContactDetailTable_bad.png)Figure: Bad Example - A too specific Contact Detail table
We normally have a general Contact Detail table that includes all the different categories of phone numbers, whether it is shared or primary plus emails all in the same table.
![ContactDetailTable_good.png](ContactDetailTable_good.png)Figure: Good Example - A general Contact Detail table
We use a Contact Detail Category table to store these categories.
![ContactDetailCategoryTable.png](ContactDetailCategoryTable.png)​
Figure: Good Example - Details of Contact Detail Category table​
