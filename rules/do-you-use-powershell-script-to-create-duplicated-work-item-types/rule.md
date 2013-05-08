---
type: rule
title: Do you use PowerShell script to create duplicated work item types?
uri: do-you-use-powershell-script-to-create-duplicated-work-item-types
created: 2012-07-18T07:41:10.0000000Z
authors:
- id: 10
  title: Lei Xu

---

 ​Sometime you will need to create duplicate work item<br>types, e.g. a task work item may be clones as PlatformDepTask, SystemDepTask;<br>both of these task work items are sharing the same fields, workflow or layouts,<br>but they are configured to be accessible by different department or there is some other minor differences.

You should create a WIT template and use a place<br>holder for the difference, e.g.<br>&lt;WORKITEMTYPE<br>name="xxxxDepNamexxxxTask"&gt;

  …<br>

&lt;/WORKITEMTYPE&gt;Figure: WIT template with place holder <br>​ 
Then use the following PowerShell script to automatically clone the work item and replace the placeholder with actual text.
​$original\_file = '..\WorkItem Tracking\TypeDefinitions\Task\_Template\_DONOTInstall.xml'

$destination\_file =  '..\WorkItem Tracking\TypeDefinitions\Task\_ PlatformDep.xml'
(Get-Content $original\_file) | Foreach-Object {
    $\_ -replace "xxxxDepNamexxxx", "PlatformDep"
    } | Set-Content $destination\_file -Encoding UTF8

$destination\_file =  '..\WorkItem Tracking\TypeDefinitions\Task\_SystemDep.xml'
(Get-Content $original\_file) | Foreach-Object {
   $\_ -replace "xxxxDepNamexxxx", "SystemDep"
   } | Set-Content $destination\_file -Encoding UTF8Figure: PowerShell script to create duplicate WITs and replace the place holder with actual data​Note: if you are using non-English characters in your<br>template, make sure you add **–Encoding UTF8 **otherwise you will have some<br>encoding problems.<br>​​​

