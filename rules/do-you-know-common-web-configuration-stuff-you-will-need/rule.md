---
type: rule
archivedreason: 
title: Do you know common web configuration stuff you will need?
guid: c0022eb0-3807-48a5-875d-5546c7ad4f8c
uri: do-you-know-common-web-configuration-stuff-you-will-need
created: 2009-06-16T01:41:30.0000000Z
authors:
- title: John Liu
  url: https://ssw.com.au/people/john-liu
- title: Jay Lin
  url: https://ssw.com.au/people/jay-lin
related: []
redirects: []

---


&#160;In SharePoint,&#160;web configuration includes&#58;
<ol>
    <li><span lang="EN-US">ASP.NET 3.5 library references – this is necessary for all the ASP.NET AJAX calls</span> </li>
    <li><span lang="EN-US">Add system.web/pages/controls – to add additional tag prefix from System.Web.Extensions</span> </li>
    <li><span lang="EN-US">Add HttpModule (for example – to clean up extra JavaScript from SharePoint)</span> </li>
    <li><span lang="EN-US">SafeControl tags for all custom dlls – in general these can be added via your solution package as well</span></li>
</ol>

<br><excerpt class='endintro'></excerpt><br>

  <p class="MsoNormal">
    <span lang="EN-US">You should always use a SPConfigModification class to modify your web.config – never tell your user or administrator to make changes manually!&#160; This also allows them to switch off a feature from SharePoint knowing that the changes had been reverted.</span>
  </p>
<span lang="EN-US" style="font-family&#58;'calibri','sans-serif';font-size&#58;11pt;">For developers – you must test your SPConfigModification carefully, mismatched XPath will cause problems in your web.config and create duplicate entries!</span>



