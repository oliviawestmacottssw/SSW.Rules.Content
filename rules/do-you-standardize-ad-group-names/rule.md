---
type: rule
title: Do you standardize AD group names?
uri: do-you-standardize-ad-group-names
created: 2015-02-16T00:13:41.0000000Z
authors:
- id: 45
  title: Chris Briggs
- id: 47
  title: Stanley Sidik

---

 
​​The use of standardised AD Group names is a simple yet crucial step, towards building a more manageable software. Raining in on the number of AD Groups will make it simpler to manage and allow new developers to pick up an existing projecting faster.
 
**​You can save yourself countless confused conversations by standardising AD Group Names.​**

For example: This is a list of AD groups associated with products.

SSWSugarLearningEvents
 SSWCodeAuditorAlerts
 SSWLinkAuditorDevs
<dd class="ssw15-rteElement-FigureBad"> 
   Figure&#58; Bad Example – It is difficult to know the correct name for an AD group​ </dd>
SSWSugarLearning
 SSWSugarLearningEvents
 SSWCodeAuditor
 SSWCodeAuditorEvents
 SSW​LinkAuditor
 SSWLinkAuditorEvents
​  <dd class="ssw15-rteElement-FigureGood"> 
   Figure&#58; Good Example – By standardising the names of AD groups it saves confusion. </dd>
It is recommend by default having two AD groups, use the following table as a guide.


| Name | Type | Purpose |
| --- | --- | --- |
| SSW&lt;ProductName&gt; | Distribution group | This email is using to send emails to the development team for a product. |
| SSW​&lt;ProductName&gt;Events | Mailbox | Acts as the collection point for all automatic notifications. For example notifications from Elmah and application insights. |

​​  
