---
type: rule
archivedreason: 
title: Do you know the best way to generate your classes from swagger?
guid: 1914ad2e-4d23-4963-9bc4-ba8d8af66070
uri: do-you-know-the-best-way-to-generate-your-classes-from-swagger
created: 2017-03-10T20:30:41.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
- title: Eric Phan
  url: https://ssw.com.au/people/eric-phan
- title: William Yin
  url: https://ssw.com.au/people/william-yin
related: []
redirects: []

---


<p class="ssw15-rteElement-P">​You can save time and reduce human error by automatically generating clients for your APIs.​<br></p>
<br><excerpt class='endintro'></excerpt><br>
<p>The best tool for this is <a href="https&#58;//github.com/RicoSuter/NSwag">NSwag</a>.<br></p><p>This is Microsoft's recommended approach, and you can read more about how to set this up in your ASP.Net Core project at <a href="https&#58;//docs.microsoft.com/en-us/aspnet/core/tutorials/getting-started-with-nswag?view=aspnetcore-3.1&amp;tabs=visual-studio">the official documentation</a>.​<br></p><p>If you use the Clean Architecture template developed by SSW's @JasonTaylorDev, this is built in out of the box. See our <a href="/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=ae1a999d-0c34-45d7-af89-7d50a9939370">rule on getting started with clean architecture</a>.<br></p><dl class="goodImage"><dt><img src="/SiteAssets/the-best-way-to-generate-your-entities-from-swagger/nswag-studio.png" alt="nswag-studio.png" style="width&#58;750px;" /></dt><dd>​​​Figure&#58; Good Example - NSwag Studio lets you customise your nswag config</dd></dl><dl class="goodImage"><dt><img src="/SiteAssets/the-best-way-to-generate-your-entities-from-swagger/jt-nswag.png" alt="jt-nswag.png" style="width&#58;750px;" /></dt><dd>Fig​​ure&#58; Good Example - @JasonTaylorDev's&#160;Clean Architecture templace comes with this built in<br></dd></dl>


