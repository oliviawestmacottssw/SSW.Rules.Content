---
type: rule
title: Do you turn on 'Development Errors' and 'Platform Tracing'?
uri: do-you-turn-on-development-errors-and-platform-tracing
created: 2012-12-10T17:51:37.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

 
When exceptions occur in CRM they are trapped by the platform layer and a standard error message is displayed to the user. At SSW we similarly implement exception handling and use [SSW Code Auditor to audit exception handling](http&#58;//www.ssw.com.au/ssw/Standards/Rules/RulesToBetterErrorhandling.aspx#CatchRethrow).

By turning DevErrors on (mainly applicable to CRM 3 and 4) you will obtain the actual error. This is what that will be posted onto newsgroups. Microsoft Support should also ask you for this information, so you probably cannot do any meaningful troubleshooting until this has been activated. To switch DevErrors on, open the web.config and change DevErrors value ="On".
![DevErrors in web.config](/SoftwareDevelopment/RulesToBetterCRMForDevelopers/PublishingImages/CRM_DevErrors.jpg)Figure: Turn on DevErrors within Web.Config file to get details of error
In CRM2011 we accomplish the same thing by turning on tracing. For more information on tracing refer to MS KB907490.

Now if all that info on the MS KS was too much, use the Diagnostics Tool for Microsoft Dynamics CRM 2011. It makes collecting trace information a snap.
![Figure&#58; Diagnostics for CRM2011](/SoftwareDevelopment/RulesToBetterCRMForDevelopers/PublishingImages/Diagnostics-for-CRM.jpg)Figure: Diagnostics for CRM2011
