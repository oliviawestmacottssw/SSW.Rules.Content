---
type: rule
title: 'MEF: Do you know not to go overboard with dynamic dependencies?'
uri: mef-do-you-know-not-to-go-overboard-with-dynamic-dependencies
created: 2012-03-21T09:45:50.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

 
Using dynamic dependencies by loading them at runtime can be useful, but it's not always required and does have some disadvantages.  You shouldn't always look to MEF to implement a dynamic strategy.

 
 
​If a reference doesn't need to be dynamically loaded at runtime, it's perfectly fine to have a default constructor that has a hardcoded instantiation of a dependency. If it was never a requirement to make that thing configurable or dynamic, don't invent business requirements just because using an IoC container is "fancier".

There are disadvantages to using dynamic loading of references:

1. You lose your Code Analysis. Only static references can be analysed by code analysis tools.
2. You lose your traceability. Visual Studio can no longer show you what concrete method is being called at design time.


c. Suggestion to MS: Currently if you use reflection, meth, unity etc… they don’t show in the dependency graph. Microsoft should support this.

For some examples of when you shouldn't use dynamic dependencies, look at these articles: [How Not to do Dependency Injection](http&#58;//www.devtrends.co.uk/blog/how-not-to-do-dependency-injection-the-static-or-singleton-container) and [Why do I need an IoC Container?](http&#58;//stackoverflow.com/questions/871405/why-do-i-need-an-ioc-container-as-opposed-to-straightforward-di-code).

