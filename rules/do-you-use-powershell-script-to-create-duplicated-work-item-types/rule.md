---
type: rule
title: Do you use PowerShell script to create duplicated work item types?
uri: do-you-use-powershell-script-to-create-duplicated-work-item-types
created: 2012-07-18T07:41:10.0000000Z
authors:
- id: 10
  title: Lei Xu

---

 
Sometime you will need to create duplicate work item types, e.g. a task work item may be clones as PlatformDepTask, SystemDepTask; both of these task work items are sharing the same fields, workflow or layouts, but they are configured to be accessible by different department or some other difference.



You should create a WIT template and use a place holder for the difference, e.g.

&lt;WORKITEMTYPE<br>name="xxxxDepNamexxxxTask"&gt;

…

&lt;/WORKITEMTYPE&gt;

Figure: WIT template with place holder
   ​$original\_file = '..\WorkItem<br>Tracking\TypeDefinitions\Task\_Template\_DONOTInstall.xml'


$destination\_file =  '..\WorkItem<br>Tracking\TypeDefinitions\Task\_ PlatformDep.xml'

(Get-Content $original\_file) | Foreach-Object {

$\_ -replace<br>"xxxxDepNamexxxx", "PlatformDep"

} | Set-Content $destination\_file<br>-Encoding UTF8



$destination\_file =  '..\WorkItem<br>Tracking\TypeDefinitions\Task\_SystemDep.xml'

(Get-Content $original\_file) | Foreach-Object {

$\_ -replace "xxxxDepNamexxxx",<br>"SystemDep"

} |<br>Set-Content $destination\_file -Encoding UTF8

Figure: PowerShell script to create duplicate WITs and replace the place holder with actual data



Note: if you are using non-English characters in your template, make sure you add **–Encoding UTF8** otherwise you will have some encoding problems.



