---
type: rule
archivedreason: 
title: Do you present the user with a nice error screen? (Web Only)
guid: 4ee8ca41-78bb-40c1-94cc-cf44a3b47622
uri: do-you-present-the-user-with-a-nice-error-screen-web-only
created: 2013-09-11T21:08:47.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 38
  title: Drew Robson
related: []
redirects: []

---

Your users should never see the “yellow screen of death” in ASP.NET. Errors should be caught, logged and a user-friendly screen displayed to the user.

<!--endintro-->

This last part is done by specifying the customErrors element in the web.config file.

This will activate ASP.NET’s built in error page (e.g. MVC’s HandleErrorAttribute filter) which can then be customized to suit your application.




> 
[[badExample]]
| ![Yellow Screen of Death](error-screen-bad.jpg)
![](error-screen-good.jpg)



:::
Figure: Good Example - Don't hide the yellow screen of death in the local environment
::: good



![](14-08-2014-2-47-50-PM-compressor.png)



However, as a developer you still want to be able to view the detail of the exception in your local development environment. Use the below setting in your Web Application's web.config file to view the yellow screen locally but present a nice error screen to the user.


Figure: Good Example - Default ASP.NET MVC custom error page
