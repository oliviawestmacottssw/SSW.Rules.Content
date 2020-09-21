---
type: rule
title: Do you control the drop down list value for Assigned To field?
uri: do-you-control-the-drop-down-list-value-for-assigned-to-field
created: 2012-07-18T07:44:27.0000000Z
authors:
- id: 10
  title: Lei Xu

---

 ​The default WIT doesn’t control the valid drop down<br>items in Assigned To filed, this will introduce unnecessary items to be shown<br>in the list which will make your users confused, e.g. TFSBUILD, tfsBuildService<br>should never be used to assign a job.
![UnnecessaryValue.png](UnnecessaryValue.png)
Figure: Bad Example – shown unnecessary values   You can add the following XML in the Assigned To filed definition to control the valid values​:​​​​​​​​​​

<FIE​LD name="Assigned To" refname="System.AssignedTo" type="String" reportable="dimension" syncnamechanges="true">
  ​<ALLOWEXISTINGVALUE />
  ​<REQUIRED />
  <ALLOWEXISTINGVALUE />
  <VALIDUSER />
  <ALLOWEDVALUES expanditems="true" filteritems="excludegroups">
        <LISTITEM value="Active" />
        <LISTITEM value="[project]\xxxxDepNamexxxxGroup" />
ALLOWEDVALUES>
FIELD>​ ​

Figure: Use ALLOWEDVALUES to control the values in Assigned to field

![ShowNecessaryUser.png](ShowNecessaryUser.png)
Figure: Good Example – shown necessary values
 ​  
