---
type: rule
archivedreason: 
title: Do you bundle all your customizations in a Solution (Model Driven)?
guid: 38997e97-94f6-4c79-9b40-f5f353227d0f
uri: do-you-bundle-all-your-customizations-in-a-solution-model-driven
created: 2020-10-28T19:00:49.0000000Z
authors:
- title: Mehmet Ozdemir
  url: https://ssw.com.au/people/mehmet-ozdemir
related: []
redirects: []

---

When customizing a Model-Driven App all changes should be in a solution. A solution holds all customization being carried out by the maker, whether it be any custom entities, processes, business rules, or modifications to existing OOTB entities.

<!--endintro-->

Solutions can be used to move these customizations between environments, eg. from development à testing à production.

Solutions can also be used to deploy changes in a managed (testing, production) and unmanaged (development) environment. Managed solutions can be thought of in simple terms and an installer can be installed and uninstalled.

Differences between Managed and Unmanaged solutions:

* When a Managed solution is uninstalled, all artifacts including data are removed
* Unmanaged solutions will install the changes but deleting the solution will leave the changes intact, so think of it as an additive change
* To completely remove all customizations in an Unmanaged solution every customized item needs to be manually deleted

<dl class="image">&lt;dt&gt;
      <img src="solutions-custom.png" alt="solutions-custom.png" style="width:750px;">
   &lt;/dt&gt;<dd>Figure: Solution show all customizations, make it very easy to move changes between environments<br></dd></dl>
### Related Rule


* [Do you create a Solution and use the "Current Environment" when creating Flow for Dynamics?](/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&TermId=d4a41d1e-6f82-4d7b-876d-87053b7b9213)