---
type: rule
title: Do you have a WitAdmin script to import work item definitions?
uri: do-you-have-a-witadmin-script-to-import-work-item-definitions
created: 2012-07-18T07:34:00.0000000Z
authors:
- id: 10
  title: Lei Xu

---

 You will need to update your work item type<br>frequently once the customization process is started, make sure you have a<br>script like below ready in your solution, this will help you to upload your<br>process template quickly with one click, it will make your development more<br>efficient. ​ECHO OFF
ECHO \*\*\*\*\*\*\*\*\*\*\*Importing new definitions\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*
ECHO ON
witadmin importwitd /collection:http://%1:8080/tfs/%2 /p:%3 /f:"..\CN.SAC.TfsProcessTemplate\WorkItem ​Tracking\TypeDefinitions\Requirement.xml"
witadmin importwitd /collection:http://%1:8080/tfs/%2 /p:%3 /f:"..\CN.SAC.TfsProcessTemplate\WorkItem Tracking\TypeDefinitions\Task.xml"
witadmin importwitd /collection:http://%1:8080/tfs/%2 /p:%3 /f:"..\CN.SAC.TfsProcessTemplate\WorkItem Tracking\TypeDefinitions\Issue.xml"

​ECHO OFF​
ECHO \*\*\*\*\*\*\*\*\*\*\*Importing new definitions\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*
ECHO ON
witadmin importwitd /collection:http://%1:8080/tfs/%2 /p:%3 /f:"..\CN.SAC.TfsProcessTemplate\WorkItem Tracking\TypeDefinitions\Requirement.xml"
witadmin importwitd /collection:http://%1:8080/tfs/%2 /p:%3 /f:"..\CN.SAC.TfsProcessTemplate\WorkItem Tracking\TypeDefinitions\Task.xml"
witadmin importwitd /collection:http://%1:8080/tfs/%2 /p:%3 /f:"..\CN.SAC.TfsProcessTemplate\WorkItem Tracking\TypeDefinitions\Issue.xml"​​ ​Figure: quick<br>deployment script for process template – Upd​ateProcessTemplate.bat With above script, you can execute the command like below UpdateProcessTemplate.bat &lt;serverAddress&gt;<br>&lt;collectionName&gt; &lt;projectName&gt;<br>​​​

