---
type: rule
title: Do you know the best way to do printable reports?
uri: do-you-know-the-best-way-to-do-printable-reports
created: 2014-01-31T00:32:32.0000000Z
authors:
- id: 38
  title: Drew Robson
- id: 45
  title: Chris Briggs

---

 Making reports on websites printable can be difficult. While there are CSS media and rules to help make pages printable, there are always issues with page breaks, browser quirks and tables.  ​
![print-reports-bad-1.png](/PublishingImages/print-reports-bad-1.png)Figure: Beautiful HTML report 
  ![print-reports-bad-2.png](/PublishingImages/print-reports-bad-2.png) Figure: Bad Example – The printed layout looks nothing like the HTML ![print-reports-bad-3.png](/PublishingImages/print-reports-bad-3.png) Figure: Beautiful PowerBI HTML report ![print-reports-bad-4.png](/PublishingImages/print-reports-bad-4.png) Figure: Bad example – PowerBI print preview scales everything down to fit on a page, you have no real control over how things flow onto multiple pages
The best and most accurate print solution is to use SQL Server Reporting Services (SSRS). You can use SQL Server Reporting Services in MVC even though its only supported by WebForms.

It's great to include  SQL Server Reporting Services (SSRS) reports in your web application, which can be done with the Microsoft ReportViewer web control...however this only applies to ASP.NET WebForms.

With an iframe and a little bit of code, your reports can also be viewed in your ASP.NET MVC application.

In your MVC project, add a new item of type WebForm.
 ![16-06-2014 10-44-12 AM.png](/PublishingImages/16-06-2014%2010-44-12%20AM.png) Figure: Add a new WebForm
Then add the ReportViewer control to the WebForm.
 ![16-06-2014 10-46-58 AM.png](/PublishingImages/16-06-2014%2010-46-58%20AM.png) Figure: Add the ReportViewer control
In the View you want to display the report in, add an iframe pointing to your WebForm.

Tie them together, by getting your report parameters from the MVC page and appending them to the query string of the iframe URL.

(The below example uses JavaScript to execute this part from user input)
 ![16-06-2014 10-50-55 AM.png](/PublishingImages/16-06-2014%2010-50-55%20AM.png) Figure: Add an iframe
Now you have your SSRS report in your MVC application.
 ![17-06-2014 8-33-37 AM.png](/PublishingImages/17-06-2014%208-33-37%20AM.png) Figure: The final report in an MVC application ![16-06-2014 10-38-51 AM.png](/PublishingImages/16-06-2014%2010-38-51%20AM.png) Figure: Export your report with the in-build SSRS functionality
### When using Web-API the method above is difficult and time-consuming!
 ![2015-04-29_10-09-56-compressor.png](/PublishingImages/2015-04-29_10-09-56-compressor.png) 
The easy solution is to render the report within the API and return it to the user  as a pdf. For an example of how to implement the functionality, read the following series  of articles on ['Integrating SSRS Web-API and AngularJS'](http&#58;//blog.chrisbriggsy.com/the-first-step-towards-integration/).

