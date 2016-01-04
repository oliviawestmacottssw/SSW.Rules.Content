---
type: rule
archivedreason: 
title: Do you know the best tools for Database Schema Update?
guid: 8d700b5d-5bc6-47ea-a3aa-025b77487475
uri: do-you-know-the-best-tools-for-database-schema-update
created: 2009-10-06T23:23:45.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
- title: Igor Goldobin
  url: https://ssw.com.au/people/igor-goldobin
- title: Adam Stephensen
  url: https://ssw.com.au/people/adam-stephensen
- title: Thiago Passos
  url: https://ssw.com.au/people/thiago-passos
- title: Brendan Richards
  url: https://ssw.com.au/people/brendan-richards
related: []
redirects: []

---


<p class="ssw15-rteElement-P">​It is important when deploying your database for the database to be updated automatically.<br></p><p class="ssw15-rteElement-P">There are a number of tools that can be used to update the database as the application can be updated.</p><div><span style="line-height&#58;21px;"><br></span></div><ul><li>Red Gate SQL Compare + Red Gate SQL Packager (post development model)<br></li><li>Visual Studio 2013​&#160;Data Dude + Deploy&#160;(post development model)<br></li><li>SQL Management Studio + OSQL&#160; (Free and roll your own)​<br></li></ul><dd class="ssw15-rteElement-FigureBad">​Figure&#58; Bad options for updating database schema​ - No ability to validate that the database hasn't been tampered with​<br></dd><div><span style="line-height&#58;21px;"><br></span></div><span style="line-height&#58;21px;"><p><img src="http&#58;//sqldeploy.com/images/SQLDeploy_logo.png" alt="" style="margin&#58;5px;" />&#160;</p><dd class="ssw15-rteElement-FigureGood">​Figure&#58; Good option for existing databases -&#160;<span style="line-height&#58;21px;">​SQL Management Studio + SSW SQL Deploy (As you go model)</span>​</dd><div><br></div><div><span style="color&#58;#ff3300;">[TODO&#58; Logo Required for SQL Validate]</span></div><p></p><dd class="ssw15-rteElement-FigureGood">​Figure&#58; Good option for when using EF&#160;Code First&#58;&#160;SSW SQL Validate<br></dd><p></p></span>

<br><excerpt class='endintro'></excerpt><br>



