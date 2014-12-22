---
type: rule
title: Do you *not* have height/width in an <img> tag?
uri: do-you-not-have-heightwidth-in-an-img-tag
created: 2014-12-22T12:28:11.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 16
  title: Tiago Araujo

---

 
The     **&lt;img&gt;** tag of HTML has 2 attributes - height and width - but any image resizing should ​be done via CSS. If the height / width ratio doesn't match that of original image, the image will be stretched.
 <dl class="badImage"><dt>
      <img src="/WebSites/RulesToBetterWebsitesLayout/PublishingImages/streched-image.jpg" alt="Stretched image which looks ugly"> 
   </dt><dd> Figure&#58; Bad example - Stretched image which looks ugly</dd></dl>
We have a program called     [SSW Code Auditor](http&#58;//www.ssw.com.au/ssw/CodeAuditor/Rules.aspx#IMGWidth) to check for this rule.

