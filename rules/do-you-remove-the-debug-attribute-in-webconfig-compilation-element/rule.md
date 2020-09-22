---
type: rule
title: Do you remove the debug attribute in Web.config compilation element?
uri: do-you-remove-the-debug-attribute-in-webconfig-compilation-element
created: 2016-08-24T22:22:22.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

 ​​The debug attribute in the web.config file is very useful for ASP.NET developers. When an error occurs the developer gets detailed error report containing the stack trace, line number and what the error is.​
 
But when debug attribute in the Web.config file is set to true it generates symbolic information (.pdb file) every time the compiler compiles your views as well as disables code optimization. So, it slows down the execution of every page.

So if you are a developer remember to remove the debug attribute and instead use custom error messages for your web pages

We have a program called [SSW Code Auditor​](https&#58;//www.ssw.com.au/ssw/codeauditor/) to check for this rule.​

​

