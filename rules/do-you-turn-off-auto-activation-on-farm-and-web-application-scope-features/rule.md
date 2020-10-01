---
type: rule
title: Do you turn off auto activation on farm and web application scope features?
uri: do-you-turn-off-auto-activation-on-farm-and-web-application-scope-features
created: 2010-04-21T12:58:32.0000000Z
authors:
- id: 8
  title: John Liu

---

Each SharePoint packages contains features that can be targetted at various scopes.  

 You need to pay special attention when you are targetting the Web Application scope.

 The feature XML looks like this.


&lt;Feature Id="{GUID}" Title="WebApplicationConfiguration" Scope="WebApplication" Version="1.0.0.0" Hidden="FALSE" DefaultResourceFile="core" xmlns="http://schemas.microsoft.com/sharepoint/" &gt;
&lt;ElementManifests /&gt;

&lt;/Feature&gt;



But there is a problem...
  The problem with this web application feature is that it will activate by default on All new Web Applications created on that farm, regardless of what the web application or root site template is.

 The best practice is to make sure you use the additional attribute ActivateOnDefault and set it to False.  Then SharePoint administrators can choose to activate the feature after a new web application is created.
  &lt;Feature Id="{GUID}" Title="WebApplicationConfiguration" Scope="WebApplication" Version="1.0.0.0" Hidden="FALSE" DefaultResourceFile="core" xmlns="http://schemas.microsoft.com/sharepoint/" 
ActivateOnDefault="False"&gt;
&lt;ElementManifests /&gt;

&lt;/Feature&gt;
