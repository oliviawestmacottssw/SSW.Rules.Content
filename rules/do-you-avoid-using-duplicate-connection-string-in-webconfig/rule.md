---
type: rule
archivedreason: 
title: Do you avoid using duplicate connection string in web.config?
guid: 0bf7e11b-1185-406d-96bd-63304f056ccb
uri: do-you-avoid-using-duplicate-connection-string-in-webconfig
created: 2009-05-11T06:55:57.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
- title: Ryan Tee
  url: https://ssw.com.au/people/ryan-tee
related: []
redirects: []

---

Since we have many ways to use Connection String in .NET 2.0, it is probably that we are using duplicate connection string in web.config.   
<!--endintro-->
<dl class="badCode">    <dt style="width&#58;92.01%;height&#58;172px;">
    <pre>&lt;connectionStrings&gt;<br>   &lt;add name=&quot;ConnectionString&quot; connectionString=&quot;Server=(local);<br>Database=NorthWind;&quot; /&gt;<br>&lt;/connectionStrings&gt;<br>&lt;appSettings&gt;<br>   &lt;add key=&quot;ConnectionString&quot; value=&quot;Server=(local);Database=NorthWind;&quot;/&gt;<br>&lt;/appSettings&gt;</pre>
    &lt;/dt&gt;
    <dd>Bad example - use duplicate connection string in web.config. </dd></dl>

| We have a program called [SSW Code Auditor](http&#58;//www.ssw.com.au/ssw/CodeAuditor/) to check for this rule. |
| --- |
