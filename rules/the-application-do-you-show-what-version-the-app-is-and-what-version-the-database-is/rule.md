---
type: rule
archivedreason: 
title: The application - Do you show what version the App is, and what version the Database is?
guid: f72682d0-f992-4021-ba50-16f394d0d2ec
uri: the-application-do-you-show-what-version-the-app-is-and-what-version-the-database-is
created: 2009-10-05T05:26:57.0000000Z
authors:
- id: 1
  title: Adam Cogan
related: []
redirects: []

---

![Everyone shows the version number somewhere on their app ...but databases also need a version number.](LinkAuditor.png)

 Let's see how to show the Database version:    
<!--endintro-->

![The applications database should have a table storing the version info](zsVersionTable.png)(the table is called \_zsDataVersion). See an example of this in[SSW Link Auditor](http://www.ssw.com.au/SSW/LinkAuditor/)
![The user can clearly see the Database version is 62 after clicking "Configure..." button in wizard "Storage Mechanism". See an example of this in](LinkAuditorVersion.png)[SSW Link Auditor](http://www.ssw.com.au/SSW/LinkAuditor/)
![The Application keeps all the scripts in a folder called SQLScripts](ChangeScripts.jpg)(this allows the application to upgrade itself and give the Reconciliation functionality)
