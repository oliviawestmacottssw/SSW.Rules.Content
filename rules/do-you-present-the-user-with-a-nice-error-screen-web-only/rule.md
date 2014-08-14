---
type: rule
archivedreason: 
title: Do you present the user with a nice error screen? (Web Only)
guid: 4ee8ca41-78bb-40c1-94cc-cf44a3b47622
uri: do-you-present-the-user-with-a-nice-error-screen-web-only
created: 2013-09-11T21:08:47.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
- title: Drew Robson
  url: https://ssw.com.au/people/drew-robson
related: []
redirects: []

---


<p>​Your users should never see the “yellow screen of death” in ASP.NET. Errors should be caught, logged and a user-friendly screen displayed to the user.</p>
<br><excerpt class='endintro'></excerpt><br>
<p>This last part is done by adding the  element to the  section of the web.config file.</p><p>This will activate ASP.NET’s built in error page (e.g. MVC’s HandleErrorAttribute filter) which can be customized to suit your application.</p><p><br></p><blockquote style="margin&#58;0px 0px 0px 40px;border&#58;none;padding&#58;0px;">​<img src="/SoftwareDevelopment/RulesForErrorHandling/PublishingImages/error-screen-bad.jpg" alt="" style="line-height&#58;20px;" /><p></p></blockquote><dl class="badImage"><dd>Figure&#58; Bad Example – Yellow Screen of Death</dd></dl><dl class="goodImage"><dt><img src="/SoftwareDevelopment/RulesForErrorHandling/PublishingImages/error-screen-good.jpg" alt="" /></dt><dd>Figure&#58; Good Example - Default ASP.NET MVC custom error page</dd><p class="ssw15-rteElement-P">​<br></p><p>​However, as a developer you still want to be able to view the detail of the exception in your local development environment. Use the below setting in your Web Application's web.config file to view the yellow screen locally but present a nice error screen to the user.<br></p><p></p><p><img src="/SoftwareDevelopment/RulesForErrorHandling/PublishingImages/Pages/present-a-nice-error-screen/14-08-2014-2-41-44-PM-compressor.png" alt="14-08-2014-2-41-44-PM-compressor.png" style="margin&#58;5px;" />​</p><dd class="ssw15-rteElement-FigureGood">Figure&#58; Good Example - Don't hide the yellow screen of death in the local environment</dd><p class="ssw15-rteElement-P"><br></p></dl>


