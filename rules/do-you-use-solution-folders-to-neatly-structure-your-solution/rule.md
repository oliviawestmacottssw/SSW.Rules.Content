---
type: rule
title: Do you use Solution Folders to Neatly Structure your Solution?
uri: do-you-use-solution-folders-to-neatly-structure-your-solution
created: 2009-04-27T08:57:42.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 17
  title: Ryan Tee

---

All the DLL references and files needed to create a setup.exe should be included in your solution. However, just including them as solution items is not enough, they will look very disordered (especially when you have a lot of solution items). And from the screenshot below, you might be wondering what the \_Instructions.docx is used for... <br> 
![-](SSW
An ideal way is to create "sub-solution folders" for the solution items, the common ones are "References" and "Setup". This will make your solution items look neat and in order. Look at the screenshot below, now it makes sense, we know that the \_Instructions.docx contains the instructions of what to do when creating a setup.exe.

![-](SSW


| We have a program called [SSW Code Auditor](http://www.ssw.com.au/ssw/CodeAuditor/Default.aspx) to check for this rule.  |
| --- |
