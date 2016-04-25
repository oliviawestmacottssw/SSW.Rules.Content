---
type: rule
archivedreason: 
title: Practices - Do you use client-side routing?
guid: 61245309-7d1c-4c21-9ba6-997f031e75e0
uri: practices-do-you-use-client-side-routing
created: 2016-04-22T22:39:45.0000000Z
authors:
- title: Steve Leigh
  url: https://ssw.com.au/people/steve-leigh
- title: Duncan Hunter
  url: https://ssw.com.au/people/duncan-hunter
related: []
redirects: []

---


<p class="p1">Single page applications (SPAs) are getting more and more popular, and for good reason – a better and faster user experience, reduced server load and encourages good API separation.</p><p class="p1">But have you ever visited a website, thought “I’ll refresh that” and then got taken back to the home screen? Or tried to copy or bookmark the URL, only to find it’s just “/Home”? This happens when client side routing hasn’t been implemented&#160;properly,&#160;and is a big hit to a site’s usability.</p>
<br><excerpt class='endintro'></excerpt><br>
<p>This is easily fixed with Angular 2’s routing capabilities, and implementing it in your SPA will confer several advantages&#58;​</p><ul><li>URLs can be copy-pasted and shared</li><li>Page refreshes work as expected</li><li>Less prone to errors</li><li>Better separation of concerns (navigation vs page state)&#160;</li></ul><dl class="badImage"><dt><img src="/PublishingImages/client-side-bad.png" alt="client-side-bad.png" /></dt><dd>Figure&#58; Bad example - The blog post component is choosing components based on the state of the component</dd></dl><p>A better way is to set up routes, and use a router (the first-party component router is great for this) to manage your components&#58;</p><dl class="goodImage"><dt><img src="/PublishingImages/client-side-good.png" alt="client-side-good.png" /></dt><dd>Good&#58; Setting up declarative routes and outlets gives a good user experience, persistent URLs and fewer moving parts </dd></dl> 


