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

The  **
![]()**  tag of HTML has 2 attributes that should not be used -  **"height"** and **"width"** .  Any image resizing should  be done via CSS. If the height / width ratio doesn't match that of original image, the image will be stretched.
 

![](images/codeauditor-logo.png)width="150" height="100" />

[[badExample]]
| ![Stretched image caused by inline height/width ratio that doesn't match](streched-image.jpg)

![](images/codeauditor-logo.png)

[[goodExample]]
| ![Avoiding inline height/width ratio keeps the image as original](non-streched-image.jpg)
We have a program called     [SSW Code Auditor](http://www.ssw.com.au/ssw/CodeAuditor/Rules.aspx#IMGWidth) to check for this rule.
