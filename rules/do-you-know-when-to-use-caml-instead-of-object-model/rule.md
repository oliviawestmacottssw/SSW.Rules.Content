---
type: rule
archivedreason: 
title: Do you know when to use CAML instead of object model?
guid: dee537be-ad13-47b4-b9e4-52fe91ba7af2
uri: do-you-know-when-to-use-caml-instead-of-object-model
created: 2009-04-09T06:10:00.0000000Z
authors:
- title: John Liu
  url: https://ssw.com.au/people/john-liu
- title: Jay Lin
  url: https://ssw.com.au/people/jay-lin
related: []
redirects: []

---


This field should not be null (Remove me when you edit this field).
<br><excerpt class='endintro'></excerpt><br>
<p>The SharePoint object model is very comprehensive and lets you select items from lists, select lists from sites, in site-collections within web-applications.</p>
<p>Naturally, using the object model is great for traversing all elements in a list.&#160; Once you have a handle to the item, you can also easily modify that item.</p>
<p>On the other hand, one of the SharePoint class SPSiteDataQuery allows a developer to use CAML to specify a query condition that SharePoint can understand to search and return matching elements from across the entire site collection.</p>
<p>This is the underlying class that the Content Query Web Part relies on.</p>
<p>So, you need to use object model when you want to&#58;</p>
<ul>
<li>Iterate all elements in a list</li>
<li>Modify elements in a list</li></ul>
<p>And you use CAML, whether in CQWP or in code with SPSiteDataQuery to&#58;</p>
<ul>
<li>Select, filter elements from SharePoint lists</li>
<li>Select elements from multiple lists</li></ul>


