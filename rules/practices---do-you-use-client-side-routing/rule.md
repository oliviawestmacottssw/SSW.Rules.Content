---
type: rule
title: Practices - Do you use client-side routing?
uri: practices---do-you-use-client-side-routing
created: 2016-04-22T22:39:45.0000000Z
authors:
- id: 55
  title: Steve Leigh
- id: 44
  title: Duncan Hunter

---

Single page applications (SPAs) are getting more and more popular, and for good reason – a better and faster user experience, reduced server load and encourages good API separation.

But have you ever visited a website, thought “I’ll refresh that” and then got taken back to the home screen? Or tried to copy or bookmark the URL, only to find it’s just “/Home”? This happens when client-side routing hasn’t been implemented properly and is a big hit to a site’s usability.
 
This is easily fixed with Angular ’s routing capabilities, and implementing it in your SPA will confer several advantages:

- URLs can be copy-pasted and shared
- Page refreshes work as expected
- Less prone to errors
- Better separation of concerns (navigation vs page state)

 [[badExample]]
| ![ The blog post component is choosing components based on the state of the component](client-side-bad.png) 
A better way is to set up routes, and use a router (the first-party component router is great for this) to manage your components:
 ![](client-side-good.png) 
Good: Setting up declarative routes and outlets gives a good user experience, persistent URLs, and fewer moving parts
