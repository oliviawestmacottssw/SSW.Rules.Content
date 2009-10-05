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


This field should not be null (Remove me when you edit this field).
<br><excerpt class='endintro'></excerpt><br>

  <p style="margin&#58;0cm 0cm 0pt;">If your project has a database, you need to select a ‘Schema Master’. This is the one person who is allowed to make modifications to the database. These include&#58;</p>
<ul>
    <li>Creating, Modifying and Deleting tables and columns </li>
    <li>Relationships </li>
    <li>Modify lookup data (see our <a href="/Standards/CodeAndApplicationDesign/RulesToBetterSQLServerSchemaDeployment/Pages/DoYouDeployLookupData.aspx">Do you deploy lookup data?</a>)<span style="text-decoration&#58;underline;"><a href="/Standards/CodeAndApplicationDesign/RulesToBetterSQLServerSchemaDeployment/Pages/DoYouDeployLookupData.aspx"> </a></span></li>
</ul>
<dl class="image">
    <dt><img alt="" src="/Standards/CodeAndApplicationDesign/RulesToBetterSQLServerSchemaDeployment/PublishingImages/SQLScriptInTFS.png" /> </dt>
    <dd>Figure&#58; The Applications Database stores version info in a table called _zsVersion </dd>
</dl>



