---
type: rule
title: Does your application's interface fit in a small screen resolution?
uri: does-your-applications-interface-fit-in-a-small-screen-resolution
created: 2012-11-27T02:02:11.0000000Z
authors: []

---

 
One side effect of having busy forms is that it doesn't scale down.
   ​
Each user prefers to have their own resolution. You must check if your controls will fit on the user's screen. Think about on which computers your application will run, and what devices will display it. To be on the safe side, it is advisable to fit your controls on an 1024 x 768px screen. Our projector has that resolution and it may well be used for presenting your application to the client.
![Bad Interface Design Example](http&#58;//www.ssw.com.au/ssw/Standards/Rules/Images/InterfaceResBadExample.jpg)Figure: Bad Example - Form is too large to fit inside 1024x768px resolution![Good Interface Design Example](http&#58;//www.ssw.com.au/ssw/Standards/Rules/Images/InterfaceResGoodExample.jpg)Figure : Good Example - Form fits inside any screen resolution
The potential solutions for this problem are:

1. Reorder and move the controls around on the form.
2. Implement Tab pages.
3. Use a wizard type interface, with Next, Back and Finish.
4. Create multiple forms each containing a subset of the controls.
5. Create a menu based form where the items are categories that some form controls fall under.
Similar to VS. Net's Tools -&gt; Options.
6. Hide unimportant controls and add the option to show them if necessary


Read our rule on[Do you design your web pages to work on 1024x768px (not 800x600px)?](http&#58;//www.ssw.com.au/ssw/Standards/Rules/RulesToBetterWebsitesLayout.aspx#Resolution) to know more.

