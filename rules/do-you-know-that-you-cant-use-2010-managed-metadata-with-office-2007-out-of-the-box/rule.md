---
type: rule
archivedreason: 
title: Do you know that you can't use 2010 Managed Metadata with Office 2007 out of the box?
guid: 6e47f490-e7cf-45ee-8dd2-f11077c947fd
uri: do-you-know-that-you-cant-use-2010-managed-metadata-with-office-2007-out-of-the-box
created: 2010-12-23T07:51:54.0000000Z
authors:
- title: John Liu
  url: https://ssw.com.au/people/john-liu
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
related: []
redirects: []

---


SharePoint 2010 and Office 2010 ships with a fantastic document management feature &quot;Managed Metadata Service&quot;. This new service provides first class support for enterprise taxonomy within a standard SharePoint 2010 environment. <br>
<br>
Unfortunately, Office 2007 and Office 2003 can't work with managed metadata fields out of the box. <br>

<br><excerpt class='endintro'></excerpt><br>
<ol>Office 2010&#58; 
   <li>Works fine </li></ol><ol>Office 2007&#58; 
   <li>Document information can't display managed metadata </li><li>You can still save documents to SharePoint </li><li>But you can't check-in (if metadata fields are required) </li><li>User needs to perform a web check-in </li></ol><ol>Office 2003&#58; 
   <li>Can't create new or Open documents with managed metadata </li><li>Install Office 2007 document support upgrade, this bring the experience a bit better similar to Office 2007. </li></ol> See more&#58;&#160;<br> 
<p style="margin&#58;0cm 0cm 0pt;">
   <span style="color&#58;black;">
      <a href="http&#58;//www.nothingbutsharepoint.com/2010/12/21/managed-metadata-columns-in-office-2007-aspx-2/" target="_blank" shape="rect">
         <font color="#0000ff" face="Calibri">http&#58;//www.nothingbutsharepoint.com/201​0/12/21/managed-metadata-columns-in-office-2007-aspx-2/</font></a> ​<br> 
      <br> </span></p><p>Best Solution&#58;<br> 
   <br> Use a 3rd party solution - the best one being OnePlaceMail which provides a UI for managed metadata via the &quot;Save to SharePoint&quot;. Works with all three versions of Office so users get a consistent UI. 
   <br> 
   <br> 
   <img class="ms-rteCustom-ImageArea" src="/SoftwareDevelopment/RulesToBetterSharePoint/PublishingImages/OnePlaceMail.jpg" alt="" /></p> 
<font class="ms-rteCustom-FigureNormal" size="+0">Figure&#58; The optional save dialog that pops up when saving document to SharePoint - allowing use of Managed Metadata from Office 2003, 2007 and File Explorer</font>


