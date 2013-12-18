---
type: rule
archivedreason: 
title: Do you use the best exception handling library?
guid: 4758ac66-d4a5-4ccd-93cc-85c1f2d369da
uri: do-you-use-the-best-exception-handling-library
created: 2013-09-11T19:17:07.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
- title: Drew Robson
  url: https://ssw.com.au/people/drew-robson
related: []
redirects: []

---


<p>​<a href="/SoftwareDevelopment/RulesForErrorHandling/Pages/use-the-best-exception-handling-framework.aspx">Do&#160;you use the best middle tier .Net libraries?</a>&#160;The best exception handling library is ELMAH.</p><p>Your users should never see the “yellow screen of death” in ASP.NET, or the “unhandled exception” message in a Windows application. Errors should always be caught and logged – preferably in a SQL database.</p>
<br><excerpt class='endintro'></excerpt><br>
<p>​<span class="s1">ELMAH is the exception logger to use for web applications. From its 
      <a href="https&#58;//www.nuget.org/packages/ELMAH"> 
         <span class="s2">NuGet page</span></a> <img title="You are now leaving SSW" src="/_LAYOUTS/15/Images/SSW/external.gif" alt="" />&#58;</span></p><p class="greyBox">
   <em>ELMAH with initial configuration for getting started quickly. ELMAH (Error Logging Modules and Handlers) is an application-wide error logging facility that is completely pluggable. It can be dynamically added to a running ASP.NET web application, or even all ASP.NET web applications on a machine, without any need for re-compilation or re-deployment.</em></p><p> 
   <strong>Note&#58; </strong>If you are still developing Windows applications, then SSW Exception Logger is the one to use. Read 
   <a href="http&#58;//www.ssw.com.au/ssw/NetToolKit/04ExceptionReporter.aspx"> 
      SSW .NET Toolkit – LadyLog User Guide</a>.</p>


