---
type: rule
archivedreason: 
title: Schema - Do you avoid using user-schema separation?
guid: bcc574f7-3dd5-45e1-8ec6-e37c434f5243
uri: schema-do-you-avoid-using-user-schema-separation
created: 2019-11-06T17:57:17.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
related: []
redirects: []

---


<p>​User-schema separation allows more flexibility​ by adding another level of naming, and shifting ownership of database objects to the schema, not the user. So, is it worth doing? Unless you are working with a very large database (100+ tables), the answer is &quot;no&quot;. Most smaller databases have all objects with owner &quot;dbo&quot;, which is fine in most cases.​<br></p>
<br><excerpt class='endintro'></excerpt><br>
<dl class="badImage"><dt>
      <img src="/PublishingImages/SQLDatabases_UserSchema_Bad.jpg" alt="SQLDatabases_UserSchema_Bad.jpg" />
   </dt><dd>​Figure&#58; Bad Example - AdventureWorks using user schema - instead, keep it simple and avoid using user schema unnecessarily</dd></dl><dl class="goodImage"><dt>
         <img src="/PublishingImages/SQLDatabases_UserSchema_Good.jpg" alt="SQLDatabases_UserSchema_Good.jpg" />​<br></dt><dd>Figure&#58; Good Example -​ Adventure works with user schema cleaned out. Much simpler and more readable​​<br></dd></dl>


