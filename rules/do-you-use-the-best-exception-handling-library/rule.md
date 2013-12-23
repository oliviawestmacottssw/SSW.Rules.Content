---
type: rule
title: Do you use the best exception handling library?
uri: do-you-use-the-best-exception-handling-library
created: 2013-09-11T19:17:07.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 38
  title: Drew Robson

---

 
​​[Do you use the best middle tier .Net libraries?](/SoftwareDevelopment/RulesForErrorHandling/Pages/use-the-best-exception-handling-framework.aspx) The best exception handling service is TFS Application Insights​. The best library is ELMAH.

Your users should never see the “yellow screen of death” in ASP.NET, or the “unhandled exception” message in a Windows application. Errors should always be caught and logged – preferably in a SQL database.
 
​At SSW we use TFS Application Insights. ​Application Insights is available as part of [Visual Studio Online​](http&#58;//msdn.microsoft.com/en-us/library/dn481095.aspx):

​     *Application Insights will tell you if your application goes down or runs slowly under load. If there are any uncaught exceptions, you’ll be able to drill into the code to pinpoint the problem. You can also find out what your users are doing with the application so that you can tune it to their needs in each development cycle.<br>*​

If TFS Application Insights is not available we use ELMAH.



ELMAH is the exception logger to use for web applications. From its <br>      [NuGet page](https&#58;//www.nuget.org/packages/ELMAH):

*ELMAH with initial configuration for getting started quickly. ELMAH (Error Logging Modules and Handlers) is an application-wide error logging facility that is completely pluggable. It can be dynamically added to a running ASP.NET web application, or even all ASP.NET web applications on a machine, without any need for re-compilation or re-deployment.*

**Note: **If you are still developing Windows applications, then SSW Exception Logger is the one to use. Read     [SSW .NET Toolkit – LadyLog User Guide](http&#58;//www.ssw.com.au/ssw/NetToolKit/04ExceptionReporter.aspx).

