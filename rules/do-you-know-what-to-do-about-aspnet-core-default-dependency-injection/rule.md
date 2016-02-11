---
type: rule
archivedreason: 
title: Do you know what to do about ASP.NET Core default dependency injection?
guid: a841c2c6-15bb-4f13-83a7-f8c201b0e937
uri: do-you-know-what-to-do-about-aspnet-core-default-dependency-injection
created: 2016-02-05T00:28:15.0000000Z
authors:
- title: Igor Goldobin
  url: https://ssw.com.au/people/igor-goldobin
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
- title: Adam Stephensen
  url: https://ssw.com.au/people/adam-stephensen
related: []
redirects: []

---


<p>​​We already know what the&#160;<a href="/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=0aa194e1-2de9-4ed1-b430-444109d65a50" style="color&#58;#cc4141;border-bottom-color&#58;#cc4141;">best IOC container is</a>, but how does ASP.NET&#160;core's default dependency injection compare​?</p><p>ASP.NET 5 includes default dependency injection for&#160;new Web Apps in the Startup.cs file. This is adequate for simple projects, but not designed to compete with the features&#160;of alternatives containers (like AutoFac's convention based registration).</p><p class="ssw15-rteElement-P">&quot;The default services container provided by ASP.NET 5 provides a&#160;minimal feature set and is not intended to replace other containers.​​&quot; - Steve Smith,&#160;(<a href="http&#58;//docs.asp.net/en/latest/fundamentals/dependency-injection.html">ASP.NET Dependency Injection</a>&#160;)</p><br>
<br><excerpt class='endintro'></excerpt><br>
<p class="ssw15-rteElement-P"><span class="ssw15-rteStyle-Highlight">You can quckly flag this error and any more by using the&#160;</span><a href="https&#58;//www.ssw.com.au/ssw/CodeAuditor/"><span class="ssw15-rteStyle-Highlight">SSW Code Auditor​</span></a><span class="ssw15-rteStyle-Highlight">.</span></p><p>Here is an example of rewiring the default code to AutoFac with the&#160;<a href="https&#58;//github.com/SSWConsulting/enterprise-musicstore-ui-angular2">SSW's Music Store​</a>&#160;&#160;app&#58;</p><dl class="ssw15-rteElement-ImageArea" style="background-color&#58;#ffffff;"><img src="/SiteAssets/do-you-know-the-best-dependency-injection-container-(aka-do-not-waste-days-evaluating-ioc-containers)/SSW-DependencyInjection-Example-Default-Bad.png" alt="SSW-DependencyInjection-Example-Default-Bad.png" style="margin&#58;5px;" /><span style="background-color&#58;initial;">&#160;​​</span><span style="background-color&#58;initial;">​​</span><dd class="ssw15-rteElement-FigureBad">Figure&#58; Bad Example -&#160;​​The default dependency injection for ASP.NET 5​<br></dd></dl><dl class="ssw15-rteElement-ImageArea" style="background-color&#58;#ffffff;">​​<img src="/SiteAssets/do-you-know-the-best-dependency-injection-container-(aka-do-not-waste-days-evaluating-ioc-containers)/SSW-DependencyInjection-Example-Default-Good.png" alt="SSW-DependencyInjection-Example-Default-Good.png" style="margin&#58;5px;width&#58;614px;height&#58;499px;" />​<br></dl><dd class="ssw15-rteElement-FigureGood">​​Figure&#58; Good Example - The bad&#160;example rewired to utilize​ AutoFac. Red boxes outline the modified code.</dd><p class="ssw15-rteElement-P">​</p><h4 style="font-size&#58;13px;">Further Reading&#58;​</h4><ul><li><a href="/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=0a5029a1-dd4f-46d7-9f22-8ab328e7c102">Do you use a dependency injection centric architecture?</a></li><li><a href="/Pages/DoYouGenerateTheVSDependencyGraph.aspx">​Do you generate the VS dependency graph?</a>​&#160;​​</li><li><p class="ssw15-rteElement-P"><a href="/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=0aa194e1-2de9-4ed1-b430-444109d65a50">Do you know the best dependency injection container? (aka Do not waste days evaluating IOC containers)​​</a></p></li></ul><p class="ssw15-rteElement-P"><br></p>


