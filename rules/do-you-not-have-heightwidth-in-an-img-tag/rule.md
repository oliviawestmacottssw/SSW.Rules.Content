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

 
The **&lt;img&gt;** tag of HTML has 2 attributes that should not be used - **"height" **and** "width"**.  Any image resizing should  be done via CSS. If the height / width ratio doesn't match that of original image, the image will be stretched.
 <dl class="badImage"><p class="ssw15-rteElement-CodeArea">&lt;img src=&quot;images/codeauditor-logo.png&quot; alt=&quot;Code Auditor logo&quot; <span class="ssw15-rteStyle-Highlight">width=&quot;150&quot; height=&quot;100&quot;</span> /&gt;​<br></p><dt>
      <img src="/PublishingImages/streched-image.jpg" alt="Stretched image which looks ugly"> 
   </dt><dd> Figure&#58; Bad example - Stretched image caused by inline​ height/width ratio that doesn't match</dd></dl><dl class="goodImage"><p class="ssw15-rteElement-CodeArea">&lt;img src=&quot;images/codeauditor-logo.png&quot; alt=&quot;Code Auditor logo&quot; &#160;/&gt;​​​​<br></p><dt>
      <img src="/PublishingImages/non-streched-image.jpg" alt="Image looks fine">​ 
   </dt><dd> Figure&#58; Good example - Avoiding inline​ height/width ratio keeps the image as original</dd></dl>
We have a program called     [SSW Code Auditor](http&#58;//www.ssw.com.au/ssw/CodeAuditor/Rules.aspx#IMGWidth) to check for this rule.

