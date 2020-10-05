---
type: rule
title: Do you use dynamic application loading in Silverlight?
uri: do-you-use-dynamic-application-loading-in-silverlight
created: 2011-05-20T02:36:18.0000000Z
authors:
- id: 8
  title: John Liu

---

​In a large business application with different and distinct modules, often it will make sense to build the separate modules and load them dynamically using a combination of Inversion of Control (IoC) and Silverlight's Dynamic Assembly Loading. <br>
   There are a few huge wins for a customer when you build your line of business application this way: 

1. The initial load isn't as large - you can have a quick load of a login and common UI, then as the person logs in, prepare their environment by loading additional components
2. You can show a quick "Do you know… you can do XXX" while this is loading. You can also show them a quick list of what has been happening (e.g. a Dashboard).
3. You can also implement special cases where perhaps HR and Finance both use the same area, but with different customizations. So based on who logs into the system, Silverlight can dynamically load a different assembly giving them a different behaviour.
4. You can also build simple "Plug-in" like functionality, allowing simple customizations of your application based on your own published interface API.


This works really well with Silverlight's Application Caching as well - and lets you build and release different component modules separately.

You can find out more about Silverlight's Dynamic Assembly Loading here:
