---
type: rule
title: Do you use Global List?
uri: do-you-use-global-list
created: 2012-07-18T07:23:54.0000000Z
authors:
- id: 10
  title: Lei Xu

---

 
Global list could be referenced in multiple work item types, if you are using the same list in different places and want to keep the drop down items consistent, global list is the best practise.
   ​​&lt;FIELD<br>name="Discipline"<br>refname="Microsoft.VSTS.Common.Discipline"<br>type="String"&gt;


<br>&lt;HELPTEXT&gt;The discipline to which the task belongs&lt;/HELPTEXT&gt;

<br>&lt;ALLOWEDVALUES expanditems="true"&gt;

<br>&lt;LISTITEM value="Development" /&gt;

<br>&lt;LISTITEM value="Test" /&gt;

<br>&lt;LISTITEM value="Project Management" /&gt;

<br>&lt;LISTITEM value="Requirements" /&gt;

<br>&lt;LISTITEM value="Architecture" /&gt;

<br>&lt;LISTITEM value="Release Management" /&gt;

<br>&lt;/ALLOWEDVALUES&gt;

&lt;/FIELD&gt;

Figure: Bad Example – embed the list items in work item type definition



&lt;?xml<br>version="1.0" encoding="utf-8"?&gt;

&lt;gl:GLOBALLISTS<br>xmlns:gl="[http://schemas.microsoft.com/VisualStudio/2005/workitemtracking/globallists](http&#58;//schemas.microsoft.com/VisualStudio/2005/workitemtracking/globallists)"&gt;

<br>&lt;GLOBALLIST<br>name="Disciplines"&gt;

<br>&lt;LISTITEM value="Architecture" /&gt;

<br>&lt;LISTITEM value="Requirements" /&gt;

<br>&lt;LISTITEM value="Development" /&gt;

<br>&lt;LISTITEM value="Release Management" /&gt;

<br>&lt;LISTITEM value="Project Management" /&gt;

<br>&lt;LISTITEM value="Test" /&gt;

<br>&lt;/GLOBALLIST&gt;

&lt;/gl:GLOBALLISTS&gt;

Figure: Good Example - Save above as GlobalList.xml file



&lt;FIELD<br>name="Discipline"<br>refname="Microsoft.VSTS.Common.Discipline" type="String"&gt;

<br>&lt;HELPTEXT&gt;The discipline to which the task belongs&lt;/HELPTEXT&gt;

<br>&lt;ALLOWEDVALUES&gt;

<br>&lt;GLOBALLIST<br>name="Disciplines" /&gt;

<br>&lt;/ALLOWEDVALUES&gt;

&lt;/FIELD&gt;

Figure: Good Example - Reference a global list in your work item type definition



Note: Global list is defined at the Team Project Collection level and it needs to be uploaded before the process template could be uploaded.

