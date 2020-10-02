---
type: rule
title: Do you know the best way to get metrics out of your browser?
uri: do-you-know-the-best-way-to-get-metrics-out-of-your-browser
created: 2019-08-27T17:42:09.0000000Z
authors:
- id: 78
  title: Matt Wicks
- id: 34
  title: Brendan Richards

---

Lighthouse is an open-source tool built into Google Chrome that can audit for performance, accessibility, progressive web apps, and more. Allowing you to improve the quality of web pages.
 
You can run Lighthouse:

- In Chrome DevTools
- From the command line
- As a Node module


It runs a series of audits against a URL and then it generates a report on how well the page did. From there, you can use the failing audits as indicators on how to improve the page. Each audit has a reference doc explaining why the audit is important, as well as how to fix it.

[[goodExample]]
| ![ Good Example - Google Chrome Lighthouse is showing 100%](lighthouse-100.png)



### Lighthouse Level 1: Throttling Off

For applications intended for use on a desktop and from within a well-connected office (such as your intranet or office timesheet application) test with throttling turned off.

### Lighthouse Level 2: Throttling On


To see how well your website would perform on low-spec devices and with poor internet bandwidth, use the throttling features. This is most important for high volume, customer-facing apps.


[[goodExample]]
| ![ Good Example - Lighhouse can simulate slow netwrking and CPU when performing tests](lighthouse_throttling.png)




### Lighthouse Level 3: Automated testing


For business-critical pages, you may want to automate Lighthouse testing as part of your Continuous Delivery pipeline. This blog post by Andrejs Abrickis shows how to configure an Azure DevOps build pipeline that performs Lighthouse testing.
[https://medium.com/@andrejsabrickis/continuously-audit-web-apps-performance-using-google-s-lighthouse-and-azure-devops-3e1623372f79](https://medium.com/%40andrejsabrickis/continuously-audit-web-apps-performance-using-google-s-lighthouse-and-azure-devops-3e1623372f79)
