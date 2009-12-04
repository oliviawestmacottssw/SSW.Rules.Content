---
type: rule
title: Do you know common web configuration stuff you will need?
uri: do-you-know-common-web-configuration-stuff-you-will-need
created: 2009-06-16T01:41:30.0000000Z
authors:
- id: 8
  title: John Liu
- id: 18
  title: Jay Lin

---

 This field should not be null (Remove me when you edit this field). 
You should always use a SPConfigModification class to modify your web.config – never tell your user or administrator to make changes manually!  This also allows them to switch off a feature from SharePoint knowing that the changes had been reverted.
For developers – you must test your SPConfigModification carefully, mismatched XPath will cause problems in your web.config and create duplicate entries!
