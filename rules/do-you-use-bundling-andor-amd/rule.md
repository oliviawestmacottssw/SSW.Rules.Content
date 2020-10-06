---
type: rule
title: Do you use Bundling and/or AMD
uri: do-you-use-bundling-andor-amd
created: 2015-06-16T07:41:41.0000000Z
authors:
- id: 34
  title: Brendan Richards
- id: 44
  title: Duncan Hunter

---

Minification and AMD are techniques to improve javascript performance. They can both can be used with vanilla JavaScript and with Typescript 
### AMD and RequireJs

AMD is a client-side technology that allows you to break you Js code into small inter-dependent modules. The modules (and thier dependencies) required to render a particular page are determined at runtime and subsequently downloaded by Javascript. RequireJs is a popular AMD implementation.
Pro: Only the js modules you need are downloadedCon: Each module is downloaded in a separate http request
### Bundling and Minification


This is a server side technique that combines and optimises client side files into single, optimised downloads.

ASP.Net contains excellent server-side bundling support as outlined here: [http://www.asp.net/mvc/overview/performance/bundling-and-minification](http&#58;//www.asp.net/mvc/overview/performance/bundling-and-minification)

ASP.Net vnext & VS 2015 also provides support for using task runners like Gulp or Grunt for bundling and minification.
Pro: Fewer Http requests and smaller filesCon: All client side modules are included in a single download
