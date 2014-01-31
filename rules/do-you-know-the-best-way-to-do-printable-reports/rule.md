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

 ​​​​​​You can use SQL Server Reporting Services in MVC even though its only supported by WebForms.​ 
​

​SQL Server Reporting Services reports can be viewed in a web page with the ReportViewer control...however this only applies to ASP.NET WebForms.

​However, with an iframe and a little bit of code, your reports can be viewed in your ASP.NET MVC application.

In your MVC project, add a new item of type WebForm.

​Add the ReportViewer control.

In the MVC view you want to display the report in, add an iframe pointing to this WebForm.

Now to tie them together, by getting your report parameters from the MVC page and appending them to the query string of the iframe URL.

