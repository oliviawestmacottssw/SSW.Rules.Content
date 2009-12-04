---
type: rule
title: Do you have a version page for your SharePoint site?
uri: do-you-have-a-version-page-for-your-sharepoint-site
created: 2009-04-20T09:20:00.0000000Z
authors:
- id: 8
  title: John Liu
- id: 1
  title: Adam Cogan

---

 This field should not be null (Remove me when you edit this field). 
![](/Standards/SoftwareDevelopment/RulesToBetterSharePoint/PublishingImages/SP_version_small.jpg)



- A custom list for Version should be created at the root level of a SharePoint site collection, and each time a package is deployed - a new record should be added to this version list.
- A simple blank page with a Content Query Web Part can display this versions list in a friendly manner.
- We do not change the version numbers in the .NET Assembly because the assemblies have to be strong-name signed and deployed to the GAC.  So having a versions list is crucial in working out what version of your package is deployed on which server.


