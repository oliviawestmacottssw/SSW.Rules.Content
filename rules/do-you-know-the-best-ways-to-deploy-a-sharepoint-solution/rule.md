---
type: rule
archivedreason: 
title: Do you know the best ways to deploy a SharePoint solution?
guid: 285249f0-a88f-448e-b1e6-17d1e0e0cee3
uri: do-you-know-the-best-ways-to-deploy-a-sharepoint-solution
created: 2009-04-17T05:39:16.0000000Z
authors:
- title: John Liu
  url: https://ssw.com.au/people/john-liu
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
related: []
redirects: []

---


This field should not be null (Remove me when you edit this field).
<br><excerpt class='endintro'></excerpt><br>
<p>The Bad method <br>The naïve and bad method would be to just back up the entire content database, then copy the database backup to the destination server, and restore it there. </p>
<ol>
<li>Backup command&#58; <br>stsadm –o backup –url http&#58;//servername&#58;port -filename c&#58;\myfile.bak </li>
<li>Restore command&#58; <br>stsadm –o restore –url http&#58;//servername&#58;port –filename c&#58;\myfile.bak -overwrite</li></ol>
<p>There are quite a few issues with this approach&#58; </p>
<ol>
<li>At a glance – seems simple </li>
<li>Any additional content at the destination server is wiped out – no content editing can continue while the development work is happening… </li>
<li>Backup file can be extremely large as it includes version history and a lot of extra fat, the file can easily be over a few hundred megabytes! </li>
<li>Deployment via backup and restore is not a Microsoft supported operation</li></ol>
<p><br>The Good method <br>The better method is to build a feature or solution deployment package </p>
<ol>
<li>Build a&#160;VSeWSS project for package and deployment </li>
<li>When built, this will produce a&#160;wsp file (this is a cab file) that can be deployed as features on the destination server </li></ol>
<p>A few considerations for this approach&#58;&#160;</p>
<ol>
<li>Site definitions, list definitions, layouts and masterpages, static content and webparts can all be deployed this way </li>
<li>User content cannot be deployed this way. Any content will need to be exported and re-imported to move between development, staging and/or production servers. </li></ol>


