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

Reflection code is often used to implement a "plugin" architecture where components are loaded at runtime rather than referenced directly in the code. This is done instead of statically referencing classes to make the solution more flexible.

The Managed Extensibility Framework (MEF) is an Inversion of Control (IoC) framework build on Reflection that simplifies and standardises this plugin methodology.

[You don't need an IoC container or ServiceLocator for everything](http&#58;//blogs.clariusconsulting.net/kzu/you-dont-need-an-ioc-or-servicelocator-for-everything/ "You don’t need an IoC container or ServiceLocator for everything"), but an IoC container WILL help if you have complex dependency graphs to instantiate (in your default constructor) or you have truly pluggable components.  For example, if you want to allow a component to be picked up automatically at runtime from some assembly if it’s in a folder.

Any existing Reflection code should be examined to see whether:

1. It needs reflection at all - can the component be directly referenced? OR
2. Can the pure reflection code be simplified with MEF?


[TODO - Damian: Bad example - using reflection]

[TODO - Damian Good Example - using MEF]
