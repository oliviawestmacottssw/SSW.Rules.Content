---
type: rule
title: Do you use hidden/visible classes when resizing to hide/show content?
uri: do-you-use-hiddenvisible-classes-when-resizing-to-hideshow-content
created: 2014-06-18T05:16:40.0000000Z
authors:
- id: 37
  title: Ben Cull

---

When designing responsive websites, it's important to consider what content is appropriate for each screen size. Desktops might have large navigation areas and extra content in a sidebar, whereas the phone might focus on other content.
 
By default, bootstrap will wrap the columns and make them full width on phones. If you want to hide content rather than let it wrap you can use the following classes:

- .hidden-xs
- .hidden-sm
- .hidden-md
- .hidden-lg


As well as being able to hide content per view, you can also selectively show it. This is helpful to add an extra sidebar for very large screens.

- .visible-xs
- .visible-sm
- .visible-md
- .visible-lg


![](RulesBootstrap - hidden.png)Bad Example: The mobile view on the right has a large unneccessary title.
Remove the title by adding the .hidden-xs class.



# ASP.NET


![](RulesBootstrap - hidden2.png)Good Example: The mobile view is now leaner and cleaner thanks to our .hidden-xs class.
