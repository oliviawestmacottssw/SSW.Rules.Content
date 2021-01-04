---
type: rule
archivedreason: 
title: Do you know how to arrange your Azure resources?
guid: 2c2f55d2-66fd-4c29-a7cb-6598c54b60df
uri: do-you-know-how-to-arrange-your-azure-resources
created: 2020-06-02T20:48:06.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
- title: Matt Wicks
  url: https://ssw.com.au/people/matt-wicks
- title: Anthony Nguyen
  url: https://ssw.com.au/people/anthony-nguyen
- title: Mehmet Ozdemir
  url: https://ssw.com.au/people/mehmet-ozdemir
related: []
redirects: []

---

There is no cost saving to group databases into on single resource group. It is better to provision the database in the same resource group as the application that uses it.

<!--endintro-->
<dl class="badImage">   &lt;dt&gt;<img src="arrange-azure-resources-bad.jpg" alt="arrange-azure-resources-bad.jpg" style="width:750px;">&lt;/dt&gt;<dd>Figure: Bad example - SSW.SQL has all the Databases for different apps in one place<br></dd></dl>
