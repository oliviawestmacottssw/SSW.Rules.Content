---
type: rule
title: The application - Do you understand the danger, and change permissions so "Schema Changes" can only be done by the "Schema Master"?
uri: the-application---do-you-understand-the-danger-and-change-permissions-so-schema-changes-can-only-be-done-by-the-schema-master
created: 2009-10-07T00:04:12.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

 This field should not be null (Remove me when you edit this field).   To avoid this problem, only one person (the "Schema Master") should have permissions to upgrade the database. ![](/Standards/CodeAndApplicationDesign/RulesToBetterSQLServerSchemaDeployment/PublishingImages/FullPermission.jpg) Figure: The db\_owner role is granted for one person only – the "Schema Master" ![](/Standards/CodeAndApplicationDesign/RulesToBetterSQLServerSchemaDeployment/PublishingImages/Adam.jpg) Figure: And here is the "Schema Master" at SSW 
