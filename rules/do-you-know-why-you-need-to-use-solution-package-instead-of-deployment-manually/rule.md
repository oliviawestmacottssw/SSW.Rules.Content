---
type: rule
title: Do you know why you need to use solution package instead of deployment manually?
uri: do-you-know-why-you-need-to-use-solution-package-instead-of-deployment-manually
created: 2009-04-09T02:44:19.0000000Z
authors:
- id: 8
  title: John Liu
- id: 18
  title: Jay Lin

---

 This field should not be null (Remove me when you edit this field). 
1. All dependent files and components are in the package - allowing developers to quickly deploy development, testing, staging and production servers.
2. Manual steps are very long, and error prone
3. Solution packages are easy to retract
4. Minimize downtime in the SharePoint production server during an upgrade operation
5. No content data loss during upgrades - SharePoint backup/restore deployment methods will block users from making changes to the production the site during the upgrade period


