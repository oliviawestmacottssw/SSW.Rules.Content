---
type: rule
title: Do you control the drop down list value for Assigned To field?
uri: do-you-control-the-drop-down-list-value-for-assigned-to-field
created: 2012-07-18T07:44:27.0000000Z
authors:
- id: 10
  title: Lei Xu

---

 
The default WIT doesn’t control the valid drop down items in Assigned To filed, this will introduce unnecessary items to be shown in the list which will make your users confused, e.g. TFSBUILD, tfsBuildService should never be used to assign a job.
![UnnecessaryValue.png](/TFS/RulesToBetterTFSCustomization/PublishingImages/UnnecessaryValue.png)

 Figure: Bad Example – shown unnecessary values
 You can add the following XML in the Assigned To filed definition to control the valid values​
   ​                &lt;FIELD name="Assigned To" refname="System.AssignedTo" type="String" reportable="dimension" syncnamechanges="true"&gt;
<br>&lt;ALLOWEXISTINGVALUE /&gt;

<br>&lt;REQUIRED/&gt;

<br>&lt;ALLOWEXISTINGVALUE /&gt;

<br>&lt;VALIDUSER/&gt;

<br>&lt;ALLOWEDVALUES expanditems="true" filteritems="excludegroups"&gt;

<br>&lt;LISTITEM value="Active" /&gt;

<br>&lt;LISTITEM value="[project]\xxxxDepNamexxxxGroup" /&gt;

<br>&lt;/ALLOWEDVALUES&gt;

<br>&lt;/FIELD&gt;

Figure: Use ALLOWEDVALUES to control the values in Assigned to field



[Good Example screen]

