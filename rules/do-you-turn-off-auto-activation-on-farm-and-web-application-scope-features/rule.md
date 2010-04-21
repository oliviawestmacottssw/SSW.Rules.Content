---
type: rule
title: Do you turn off auto activation on farm and web application scope features?
uri: do-you-turn-off-auto-activation-on-farm-and-web-application-scope-features
created: 2010-04-21T12:58:32.0000000Z
authors:
- id: 8
  title: John Liu

---

 This field should not be null (Remove me when you edit this field).   The problem with this web application feature is that it will activate by default on All new Web Applications created on that farm, regardless of what the web application or root site template is.

 The best practice is to make sure you use the additional attribute ActivateOnDefault and set it to False.  Then SharePoint administrators can choose to activate the feature after a new web application is created.
  &lt;Feature Id="{GUID}" Title="WebApplicationConfiguration" Scope="WebApplication" Version="1.0.0.0" Hidden="FALSE" DefaultResourceFile="core" xmlns="[http://schemas.microsoft.com/sharepoint/](http&#58;//schemas.microsoft.com/sharepoint/)" ActivateOnDefault="False"&gt;
&lt;ElementManifests /&gt;

&lt;/Feature&gt;



