---
type: rule
title: How do you deploy SharePoint?
uri: how-do-you-deploy-sharepoint
created: 2009-03-30T00:44:00.0000000Z
authors: []

---

 This field should not be null (Remove me when you edit this field). 
Our answer to the deployment problem is a combination of tools and processes – we call it the SSWpackage.exe

- **Multiple development virtual machine environments
**
    - Test repeated deployment to staging before you actually deploy to the production server
- **SSW SharePoint Deployment Auditor** – compares development, staging and production servers to identify missing files that needs to be deployed
    - Specify ignore lists
    - Spits out XML code that would be easy to add to your package xml
- **SSW Package Updater** – updates the solution package based on the XML definitions
    - Ensure you always have the latest version of the files from development SharePoint included in your package.
- **Microsoft Visual Studio **extensions for Windows SharePoint Services
    - Using the latest VSeWSS 1.3 CTP
    - Generates the package and batch files
- **SharePoint STSADM** tool for deployment


Into the future of SSWPackage.exe

- Fully continuous integration with SharePoint
- More SharePoint validation functions
- Improved versioning control
- A great GUI to bring it all together


