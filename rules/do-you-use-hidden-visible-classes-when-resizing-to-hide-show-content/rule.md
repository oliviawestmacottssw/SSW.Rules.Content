---
type: rule
archivedreason: 
title: Do you use hidden/visible classes when resizing to hide/show content?
guid: 516a0486-d6d5-4ca2-9171-356115874c60
uri: do-you-use-hidden-visible-classes-when-resizing-to-hide-show-content
created: 2014-06-18T05:16:40.0000000Z
authors:
- title: Ben Cull
  url: https://ssw.com.au/people/ben-cull
related: []
redirects: []

---

When designing responsive websites, it's important to consider what content is appropriate for each screen size. Desktops might have large navigation areas and extra content in a sidebar, whereas the phone might focus on other content.

<!--endintro-->

By default, bootstrap will wrap the columns and make them full width on phones. If you want to hide content rather than let it wrap you can use the following classes:

* .hidden-xs
* .hidden-sm
* .hidden-md
* .hidden-lg


As well as being able to hide content per view, you can also selectively show it. This is helpful to add an extra sidebar for very large screens.

* .visible-xs
* .visible-sm
* .visible-md
* .visible-lg

<dl class="badImage">&lt;dt&gt; 
      <img src="RulesBootstrap - hidden.png" alt="RulesBootstrap - hidden.png" style="margin:5px;width:550px;"> 
   &lt;/dt&gt;<dd>Bad Example: The mobile view on the right has a large unneccessary title.</dd></dl>
Remove the title by adding the .hidden-xs class.



# ASP.NET

<dl class="goodImage">   &lt;dt&gt; 
      <img src="RulesBootstrap - hidden2.png" alt="RulesBootstrap - hidden2.png" style="margin:5px;width:550px;"> 
   &lt;/dt&gt;<dd>Good Example: The mobile view is now leaner and cleaner thanks to our .hidden-xs class.</dd></dl>
