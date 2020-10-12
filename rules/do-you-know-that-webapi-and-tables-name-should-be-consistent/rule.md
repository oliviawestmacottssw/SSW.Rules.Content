---
type: rule
title: Do you know that WebAPI and tables name should be consistent?
uri: do-you-know-that-webapi-and-tables-name-should-be-consistent
created: 2015-04-28T13:30:47.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

When creating WebAPIs for your applications, it is useful to keep the naming consistent all the way from the back-end to the front-end. 
[greyBox]
  **Table name:**  Employees
 **Endpoint:**  /api/Users
 
[/greyBox]
Bad Example: The endpoint is different to the table name




[greyBox]
  **Table name:**  Employees
 **Endpoint:**  /api/Employees
 
[/greyBox]

Good Example: Table name is the same as the WebAPI endpoint


By making the endpoint the same as the table name, you can simplify development and maintenance of the WebAPI layer.

In some circumstances you may not have direct control over the database however. In these situations it may make sense to have different endpoint names if doing so will simplify development for consumers of your WebAPI endpoints.
