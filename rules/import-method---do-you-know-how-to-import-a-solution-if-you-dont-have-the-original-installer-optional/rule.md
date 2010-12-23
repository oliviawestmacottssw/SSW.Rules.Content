---
type: rule
title: Import Method - Do you know how to import a solution if you don’t have the original installer? (optional)
uri: import-method---do-you-know-how-to-import-a-solution-if-you-dont-have-the-original-installer-optional
created: 2010-12-23T03:10:35.0000000Z
authors: []

---

 You should have at this point, either:

<br>1. Installer packages from 3rd Party Vendors for installing their custom solution or,
<br>2. WSP packages from 3rd party, or built from your own source code, or extracted using the Export Method (not recommended)

<br>You can add the WSP package solutions to the new server by:<br>
1. Open up **cmd** with Administrator privileges
2. Enter your **C:\SharePointCustomizations **folder
cd C:\SharePointCustomizations
3. Use **stsadm** to import the solution to your new server
Stsadm –o AddSolution –filename NameOfSolution.wsp
4. Make sure there are no errors when the command runs


