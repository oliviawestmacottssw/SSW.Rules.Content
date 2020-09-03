---
type: rule
archivedreason: 
title: Do you create a Solution and use the "Current Environment" when creating Flow for Dynamics?
guid: 1161e28b-130b-4401-947d-0037f61b877a
uri: do-you-create-a-solution-and-use-the-current-environment-when-creating-flow-for-dynamics
created: 2020-06-25T22:11:47.0000000Z
authors:
- title: Mehmet Ozdemir
  url: https://ssw.com.au/people/mehmet-ozdemir
related: []
redirects: []

---

When creating workflows in Dynamics developers take for granted when a solution file is moved across environments, things just work. To achieve the same with Flows we need to make sure that when connecting to Dynamics using the Comm Data Service connector, we in fact connect with Common Data Service (Current Environment) connector. This connector is environmentally aware and will immediately work when the parent solution is deployed to another environment, it doesn't require any post-deployment steps.

<!--endintro-->

**Tip:** When searching for Common Data Services (Current Environment) it’s very easy to pick the wrong one:
<dl class="image">&lt;dt&gt; 
      <img src="common-data-services.png" alt="common-data-services.png">       
   &lt;/dt&gt;</dl>
### Related Rule

* [Do you bundle all your customizations in a Solution (Model-Driven)?](/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&TermId=70032aa5-72c9-447b-9cab-bf862401ad06)