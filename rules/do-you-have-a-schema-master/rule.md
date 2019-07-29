---
type: rule
archivedreason: 
title: Do you have a "Schema Master"?
guid: c40124b5-f5e9-4f6c-8085-e3b91e645379
uri: do-you-have-a-schema-master
created: 2009-10-05T05:51:48.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
related: []
redirects: []

---


You have a web site master right? This is the central point of contact if the site goes down.<br>
When developing an application, all members can code. However schema changes being done by many developers often can lead to trouble. <br>
<br>
Who&#160;is &quot;Schema Master&quot;? What does he do? 

<br><excerpt class='endintro'></excerpt><br>

  <dl class="image">
    <dt><img src="/PublishingImages/Nick.png" alt="" /> </dt>
    <dd>Figure&#58; One person should be the 'Schema Master', on an average sized project (of 5-10 devs) </dd>
</dl>
<p style="margin&#58;0cm 0cm 0pt;">If your project has a database, you need to select a &quot;Schema Master&quot;. This is the one person who should review all&#160;modifications to the database. These include&#58;</p>
<ul>
    <li>Creating, Modifying and Deleting tables and columns </li>
    <li>Relationships </li>
    <li>Modify <a href="/Pages/DoYouDeployLookupData.aspx">Controlled Lookup Data</a> </li>
</ul>
The &quot;Schema Master&quot; in a development shop is often the lead programmer on the team. They are&#160;in charge of all database changes and scripts. Team members should still feel free to make changes, just get them double checked by the Schema Master.<dl class="image">
    <dt><img src="/PublishingImages/zsVersionTable.png" alt="" /> </dt>
    <dd>Figure&#58; The Applications Database stores version info in a table called _zsVersion </dd>
</dl>
<dl class="image">
    <dt><img src="/PublishingImages/SQLScriptInTFS.png" alt="" /> </dt>
    <dd>Figure&#58; Only a &quot;Schema Master&quot; checks in the .sql files </dd>
</dl>



