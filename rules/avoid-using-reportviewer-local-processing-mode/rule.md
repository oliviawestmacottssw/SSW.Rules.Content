---
type: rule
archivedreason: 
title: Do you avoid using ReportViewer local processing mode?
guid: d18272f4-c4b7-4d7b-be6a-b9729503615d
uri: avoid-using-reportviewer-local-processing-mode
created: 2016-11-11T18:00:54.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
related: []
redirects:
- do-you-avoid-using-reportviewer-local-processing-mode

---


<p><a href="https&#58;//www.ssw.com.au/ssw/redirect/msdn/ReportViewerControl.htm">ReportViewer control</a>&#160;is a powerful control designed for Windows application and Web application to process and display reports. This control can be configured to run in local processing mode and remote processing mode.​​​<br></p>
<br><excerpt class='endintro'></excerpt><br>
<ul><li>​Local Processing Mode<br>This mode uses&#160;<a href="https&#58;//www.ssw.com.au/ssw/redirect/msdn/CreatingClientReportDefinition.htm">client report definition (.rdlc) files</a>, all report processing is performed on the computer that hosts the application. All data used by the report must be retrieved from data that the client application provides, so you have to configure the ReportViewer control's Data sources, Report parameters.<br>See&#160;<a href="https&#58;//www.ssw.com.au/ssw/redirect/msdn/ConfiguringReportViewer.htm">Configuring ReportViewer for Local Processing</a>&#160;for more information.</li><li>Remote Processing Mode<br>This mode needs the Microsoft SQL Server 2005 Reporting Services report server, The report server processes the data and renders the report into an output format. The ReportViewer control retrieves the finished report from the report server and displays it on the screen, so you have to configure the ReportViewer control's report server information.&#160;<br>See&#160;<a href="https&#58;//www.ssw.com.au/ssw/redirect/msdn/ConfiguringReportViewerforRemotProcessing.htm">Configuring ReportViewer for Remote Processing</a>&#160;for more information.</li></ul><p>If you use local processing mode in your Web application, there are more configuration to do for the ReportViewer control, report processing will also slow down the web server. </p><p><br></p>


