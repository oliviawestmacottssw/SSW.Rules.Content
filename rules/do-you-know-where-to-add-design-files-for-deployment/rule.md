---
type: rule
archivedreason: 
title: Do you know where to add design files for deployment?
guid: fa61b04c-a32c-4b7d-a8e3-f260d158af0f
uri: do-you-know-where-to-add-design-files-for-deployment
created: 2009-04-20T00:13:00.0000000Z
authors:
- title: John Liu
  url: https://ssw.com.au/people/john-liu
related: []
redirects: []

---


This field should not be null (Remove me when you edit this field).
<br><excerpt class='endintro'></excerpt><br>
<p>So our rules are&#58;</p>
<ol>
<li>Never modify out of the box SharePoint files in /Style Library/ -&#160;those files are part of the site definition, if you customize them they are hard to deploy</li>
<li>Start with a clean, minimal masterpage</li>
<li>Create and reference&#160;your own CSS files and put them&#160;under /Style Library/CSS/&lt;client&gt;/</li>
<li>You may want to further divide your CSS paths according to the areas of the site that your CSS is designed for&#58;<br>E.g. /Style Library/CSS/SSW/Clients/layout.css</li>
<li>Designers can modify the XSL file as well!<br>put them under /Style Library/XSL Style Sheets/&lt;client&gt;/</li></ol>


