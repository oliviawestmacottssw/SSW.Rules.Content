---
type: rule
title: Do you do know the best technical solution to enable purchase approvals?
uri: do-you-do-know-the-best-technical-solution-to-enable-purchase-approvals
created: 2013-04-19T19:04:02.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 4
  title: Ulysses Maclaren

---

 
This is quintessential workflow and online forms. Basically you have purchase requests, then business rules, then approvals.
 E.g. Less than $1K your direct manager can approve.
 
Choices:- **TFS 2012** (too hard)
 You can have requests go in as a work items but there is no workflow service that runs on the server, so the workflow would have to be in a separate web service using WF4.
- **SharePoint 2013** (recommended)
 SharePoint needs an out of the box solution. You can have requests go into SharePoint lists and then there is a workflow service that runs on the server, using WF3 under the covers.
- **CRM 2011**
 CRM also needs an out of the box solution. You can have requests go into as CRM Entities and there is a workflow service that runs on the server, using WF3 under the covers.
- **JIRA**
 Jira supports workflows and approvals (non .NET)


