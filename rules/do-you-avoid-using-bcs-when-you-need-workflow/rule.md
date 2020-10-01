---
type: rule
title: Do you avoid using BCS when you need Workflow?
uri: do-you-avoid-using-bcs-when-you-need-workflow
created: 2010-06-04T06:39:12.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

If you are planning to use Workflow, use Workflow with SharePoint List instead of BCS. Because Workflow cannot be associated directly with external lists. The reason is data is not stored in SharePoint, so the Workflow cannot be notified when items change.


![](BCSDoesNotSupportWF.jpg)
BCS doesn't have WorkFlow support


![](WFSupportList.jpg)
Use WorkFlow with SharePoint List
