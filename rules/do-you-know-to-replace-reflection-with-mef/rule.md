---
type: rule
title: Do you know to replace reflection with MEF?
uri: do-you-know-to-replace-reflection-with-mef
created: 2012-03-21T01:47:46.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 23
  title: Damian Brady

---

 
a.      You don’t want containers ????


[You don’t need an IoC container or ServiceLocator for everything](http&#58;//blogs.clariusconsulting.net/kzu/you-dont-need-an-ioc-or-servicelocator-for-everything/ "You don’t need an IoC container or ServiceLocator for everything")


An IoC container WILL help if you have complex dependency graphs to instantiate (in your default constructor) or you have truly pluggable components (i.e. you want to allow a component to be picked up automatically at runtime from some binary if it’s in a folder, etc.).

If you don’t, it’s perfectly fine to have a default constructor that is used at runtime and has a hardcoded instantiation of a dependency. It was never a requirement to make that thing configurable or dynamic. So don’t invent business requirements just ‘cause using an IoC container is fancier. ​



[[http://www.devtrends.co.uk/blog/how-not-to-do-dependency-injection-the-static-or-singleton-container](http&#58;//www.devtrends.co.uk/blog/how-not-to-do-dependency-injection-the-static-or-singleton-container)]

[[http://stackoverflow.com/questions/871405/why-do-i-need-an-ioc-container-as-opposed-to-straightforward-di-code](http&#58;//stackoverflow.com/questions/871405/why-do-i-need-an-ioc-container-as-opposed-to-straightforward-di-code)]










b.      You don’t want reflection ….. much better to use meth
<br>​ 
