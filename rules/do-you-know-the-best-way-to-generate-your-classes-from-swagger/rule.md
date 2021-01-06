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

You can save time and reduce human error by automatically generating clients for your APIs.

<!--endintro-->

The best tool for this is [NSwag](https://github.com/RicoSuter/NSwag).

This is Microsoft's recommended approach, and you can read more about how to set this up in your ASP.Net Core project at [the official documentation](https://docs.microsoft.com/en-us/aspnet/core/tutorials/getting-started-with-nswag?view=aspnetcore-3.1&tabs=visual-studio).

If you use the Clean Architecture template developed by SSW's @JasonTaylorDev, this is built in out of the box. See our [rule on getting started with clean architecture](/Clean-Architecture-the-best-way-to-get-started).
<dl class="goodImage"><dt><img src="nswag-studio.png" alt="nswag-studio.png" style="width:750px;"></dt><dd>Figure: Good Example - NSwag Studio lets you customise your nswag config</dd></dl><dl class="goodImage"><dt><img src="jt-nswag.png" alt="jt-nswag.png" style="width:750px;"></dt><dd>Figure: Good Example - @JasonTaylorDev's Clean Architecture templace comes with this built in<br></dd></dl>
