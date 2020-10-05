---
type: rule
title: Do you know how to add a version number to setup package in Advanced Installer?
uri: do-you-know-how-to-add-a-version-number-to-setup-package-in-advanced-installer
created: 2014-09-18T20:02:53.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 46
  title: Danijel Malik

---

​Developers should add a version number at the end of the out package. E.g. SSWCodeAuditor\_v14.0.0.exe

Here is how you do it in Advanced Installer:
 
1. ​In the navigation pane look for <br>      **Media**
2. Choose <br>      **Configuration** tab and click in <br>      **MSI name** text box which is located under <br>      **Output** section
3. Next to the text add <br>      [|ProductVersion]. If the text-box is empty you may want to start it with <br>      [|ProductName]


![](installer-add-version-number.jpg)Figure​: Advanced Installer - Add version to output package
