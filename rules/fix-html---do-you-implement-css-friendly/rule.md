---
type: rule
title: Fix HTML - Do you implement CSS friendly?
uri: fix-html---do-you-implement-css-friendly
created: 2009-06-16T01:52:11.0000000Z
authors:
- id: 8
  title: John Liu
- id: 18
  title: Jay Lin

---

 This field should not be null (Remove me when you edit this field). 
When you first run your SharePoint site – you’ll discover that it looks nice on the surface but needs a significant amount of work to fix all the bad HTML.

Implement CSS Friendly – these are the control adapters released by Microsoft to make ASP.NET render better, non-table based controls.  You can implement them for SharePoint sites as well.
&lt;TABLE id=zz1\_TopNavigationMenu class="..." border=0 cellSpacing=0 cellPadding=0&gt;
&lt;TBODY&gt;
    &lt;TR&gt;
    &lt;TD id=zz1\_TopNavigationMenun0&gt;
        &lt;TABLE class="..." border=0 cellSpacing=0 cellPadding=0 width="100%"&gt;
        &lt;TBODY&gt;
            &lt;TR&gt;
                &lt;TD style="WHITE-SPACE: nowrap"&gt;
                &lt;A style="..." class="..." href="..."&gt;Home&lt;/A&gt;
                &lt;/TD&gt;
            &lt;/TR&gt;
        &lt;/TBODY&gt;
        &lt;/TABLE&gt;
    &lt;/TD&gt;
    ...   
    &lt;TD id=zz1\_TopNavigationMenun1&gt;
        &lt;TABLE class="..." border=0 cellSpacing=0 cellPadding=0 width="100%"&gt;
        &lt;TBODY&gt;
            &lt;TR&gt;
                &lt;TD style="WHITE-SPACE: nowrap"&gt;
                &lt;A style="..." class="..." href="..."&gt;Operations&lt;/A&gt;
                &lt;/TD&gt;
            &lt;/TR&gt;
        &lt;/TBODY&gt;
        &lt;/TABLE&gt;
    &lt;/TD&gt;
    ...
    &lt;TD id=zz1\_TopNavigationMenun2&gt;
        &lt;TABLE class="..." border=0 cellSpacing=0 cellPadding=0 width="100%"&gt;
        &lt;TBODY&gt;
            &lt;TR&gt;
                &lt;TD style="WHITE-SPACE: nowrap"&gt;
                &lt;A style="..." class="..." href="..."&gt;Application Management&lt;/A&gt;
                &lt;/TD&gt;
            &lt;/TR&gt;
        &lt;/TBODY&gt;
        &lt;/TABLE&gt;
    &lt;/TD&gt;
    ...
    &lt;/TR&gt;
&lt;/TBODY&gt;
&lt;/TABLE&gt;Bad example - without using CSS Friendly &lt;div class="CssFriendly-Menu-Horizontal" id="zz1\_TopNavigationMenu"&gt;
    &lt;ul class="CssFriendly-Menu"&gt;
        &lt;li class="CssFriendly-Menu-WithChildren"&gt;
        &lt;a href="..." class="CssFriendly-Menu-Link TopLevelNavItem"&gt;About Us&lt;/a&gt;
        &lt;div class="cbb CssFriendly-Menu-Dropdown"&gt;
            &lt;div class="CssFriendly-Menu-Dropdown-ItemHost"&gt;
                &lt;ul class="first"&gt;
                    &lt;li class="CssFriendly-Menu-Leaf"&gt;
                    &lt;a href="..." class="CssFriendly-Menu-Link"&gt;Employees&lt;/a&gt;
                    &lt;/li&gt;
                &lt;/ul&gt;
            &lt;/div&gt;
        &lt;/div&gt;
        &lt;/li&gt;
        ...
    &lt;/ul&gt;
&lt;/div&gt; Good example - using CSS Friendly


