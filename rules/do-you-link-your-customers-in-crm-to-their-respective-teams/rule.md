---
type: rule
title: Do you link your customers in CRM to their respective Teams?
uri: do-you-link-your-customers-in-crm-to-their-respective-teams
created: 2020-03-27T21:55:12.0000000Z
authors:
- id: 69
  title: Jean Thirion
- id: 78
  title: Matt Wicks

---

 
If you use a Team per client, it is likely that you want to have a link between your Teams instances and the associated CRM record.​​
 
​At SSW we have a custom property for each client that stores the Teams URL:​​​
![live-crm.jpg](live-crm.jpg)Figure: Live CRM | Company/Account Form – added Teams URL field
To get that URL, simply click the ellipsis next to your Team name and click "Get link to Team"
![get-teams-url.jpg](get-teams-url.jpg)Figure: get the Teams URL
This process can even be automated using Azure functions and Graph API to provision a new Team every time a new client is created in CRM.

