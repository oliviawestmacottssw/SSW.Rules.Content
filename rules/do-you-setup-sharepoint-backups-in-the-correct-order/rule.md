---
type: rule
title: Do you setup SharePoint backups in the correct order?
uri: do-you-setup-sharepoint-backups-in-the-correct-order
created: 2011-06-15T00:50:23.0000000Z
authors:
- id: 21
  title: Matthew Hodgkins

---

 DPM is great for backing up SharePoint data, but when you select to back up the SharePoint role of a server, DPM will only backup the SharePoint\_Config database and the content databases, which is less than ideal.<br>   To back up the SharePoint Server properly in DPM: 




1. Create a new Protection Group, for our example we will call it SharePoint Protection
2. In the new Protection Group, add protection for the for the SharePoint role on your SharePoint server:



