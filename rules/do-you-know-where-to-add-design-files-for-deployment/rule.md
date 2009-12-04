---
type: rule
title: Do you know where to add design files for deployment?
uri: do-you-know-where-to-add-design-files-for-deployment
created: 2009-04-20T00:13:00.0000000Z
authors:
- id: 8
  title: John Liu

---

 This field should not be null (Remove me when you edit this field). 
So our rules are:

1. Never modify out of the box SharePoint files in /Style Library/ - those files are part of the site definition, if you customize them they are hard to deploy
2. Start with a clean, minimal masterpage
3. Create and reference your own CSS files and put them under /Style Library/CSS/&lt;client&gt;/
4. You may want to further divide your CSS paths according to the areas of the site that your CSS is designed for:
E.g. /Style Library/CSS/SSW/Clients/layout.css
5. Designers can modify the XSL file as well!
put them under /Style Library/XSL Style Sheets/&lt;client&gt;/


