---
type: rule
title: Do you know how to set up Application Insights?
uri: do-you-know-how-to-set-up-application-insights
created: 2015-07-24T04:48:34.0000000Z
authors:
- id: 45
  title: Chris Briggs

---

 
​​​The easiest way to get started with Application Insights is to follow the documentation on MSDN [https://azure.microsoft.com/en-us/documentation/articles/app-insights-get-started/](https&#58;//azure.microsoft.com/en-us/documentation/articles/app-insights-get-started/) 
Below are our additional suggestions to help you get the most out of Application Insights.


 
**High level summary of setup**
Application Insights requires that you make 2 general modifications to your application:
1. Manually add a Javascript tracker to your web page header (can be done through master page), this modification enables the "browser page loading time" monitor and can track client side exceptions:
![app-insights-browser-loading-time.jpg](/SiteAssets/application-insights-in-sharepoint/app-insights-browser-loading-time.jpg)
2. Add Application Insights DLL references and update web.config, these modifications enable the "server response time", "server request" and "failed requests" monitors. 
This is usually done via the tools within Visual Studio, but can be done via the server monitoring tool to an ASP.Net application you don't have control over (e.g. SharePoint).
![server-response-requests-failed-requests.jpg](/SiteAssets/application-insights-in-sharepoint/server-response-requests-failed-requests.jpg)





**Tip #1 – Add enhanced Exception tracking to your application**
The default set up and configuration of Application Insights will send generic performance stats and Exceptions. If you will be using Application Insights to look deeper into these Exceptions then it is important to make sure the full stack trace is sent when Exceptions occur. This can be added to your application by adding code for all unhandled exceptions. Follow this documentation page for more information [https://azure.microsoft.com/en-us/documentation/articles/app-insights-asp-net-exceptions/](https&#58;//azure.microsoft.com/en-us/documentation/articles/app-insights-asp-net-exceptions/)

**Tip #2 – Add Web tests to monitor performance metrics over time
**As soon as you have configured Application Insights, you should immediately add a web test to track the general performance trends ​​over time. More information can be found at this rule &lt;Rule coming soon&gt;

**Tip #3 – You can add monitoring to ASP.Net applications you have deployed but don't have source control access over**
This rule on how to add Application Insights to a SharePoint application shows that you can use the Application Insights monitor to add the .dlls and modify the web.config file of a deployed application https://rules.ssw.com.au/application-insights-in-sharepoint​

