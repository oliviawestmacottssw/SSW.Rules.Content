---
type: rule
archivedreason: 
title: Do you store Application-Level Settings in your database rather than configuration files when possible?
guid: c05a82d9-f7ac-4716-ae68-b85ae83e88ce
uri: do-you-store-application-level-settings-in-your-database-rather-than-configuration-files-when-possible
created: 2018-04-26T21:16:04.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
related: []
redirects: []

---


For database applications, it is best to keep application-level values (apart from connection strings) from this in the database rather than in the web.config.&#160; There are some merits as following&#58;<br><br>
<br><excerpt class='endintro'></excerpt><br>
<ol><li>It can be updated easily with normal SQL e.g. Rolling over the current setting to a new value.<br></li><li>It can be used in joins and in other queries easily without the need to pass in parameters.</li><li>It can be used to update settings and affect the other applications based on the same database.​​<br></li></ol>


