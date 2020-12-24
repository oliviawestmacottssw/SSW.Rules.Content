---
type: rule
archivedreason: 
title: Fix HTML - Do you implement CSS friendly?
guid: d19badb1-94f3-48c9-8409-d562a857b407
uri: fix-html-do-you-implement-css-friendly
created: 2009-06-16T01:52:11.0000000Z
authors:
- id: 8
  title: John Liu
- id: 18
  title: Jay Lin
related: []
redirects: []

---

It is extremely important to make your site standards compliant:

* It makes styling a lot easier.
* It also means your site is likely to work for all browsers, even if you don’t specifically target/support them.
* It requires accessibility for big public sites can be met easier.


<!--endintro-->

When you first run your SharePoint site – you’ll discover that it looks nice on the surface but needs a significant amount of work to fix all the bad HTML.

Implement CSS Friendly – these are the control adapters released by Microsoft to make ASP.NET render better, non-table based controls.  You can implement them for SharePoint sites as well.
 &lt;&lt;/TABLE&gt;
&lt;/TBODY&gt;
    &lt;/TR&gt;
    ...
    &lt;/TD&gt;
        &lt;/TABLE&gt;
        &lt;/TBODY&gt;
            &lt;/TR&gt;
                &lt;/TD&gt;
                &lt;A style="..." class="..." href="..."&gt;Application Management&lt;/A&gt;
                &lt;TD style="WHITE-SPACE: nowrap"&gt;
            &lt;TR&gt;
        &lt;TBODY&gt;
class="..." border=0 cellSpacing=0 cellPadding=0 width="100%"&gt;<font style="background-color&#58;rgb(255, 255, 128);">TABLE </font>        &lt;
    &lt;TD id=zz1\_TopNavigationMenun2&gt;
    ...
    &lt;/TD&gt;
        &lt;/TABLE&gt;
        &lt;/TBODY&gt;
            &lt;/TR&gt;
                &lt;/TD&gt;
                &lt;A style="..." class="..." href="..."&gt;Operations&lt;/A&gt;
                &lt;TD style="WHITE-SPACE: nowrap"&gt;
            &lt;TR&gt;
        &lt;TBODY&gt;
class="..." border=0 cellSpacing=0 cellPadding=0 width="100%"&gt;<font style="background-color&#58;rgb(255, 255, 128);">TABLE </font>        &lt;
    &lt;TD id=zz1\_TopNavigationMenun1&gt;
    ...   
    &lt;/TD&gt;
        &lt;/TABLE&gt;
        &lt;/TBODY&gt;
            &lt;/TR&gt;
                &lt;/TD&gt;
                &lt;A style="..." class="..." href="..."&gt;Home&lt;/A&gt;
                &lt;TD style="WHITE-SPACE: nowrap"&gt;
            &lt;TR&gt;
        &lt;TBODY&gt;
class="..." border=0 cellSpacing=0 cellPadding=0 width="100%"&gt;<font style="background-color&#58;rgb(255, 255, 128);">TABLE </font>        &lt;
    &lt;TD id=zz1\_TopNavigationMenun0&gt;
    &lt;TR&gt;
&lt;TBODY&gt;
id=zz1\_TopNavigationMenu class="..." border=0 cellSpacing=0 cellPadding=0&gt;<font style="background-color&#58;rgb(255, 255, 128);">TABLE </font>Bad example - without using CSS Friendly &lt;div class="CssFriendly-Menu-Horizontal" id="zz1\_TopNavigationMenu"&gt;&lt;/div&gt;
    &lt;/ul&gt;
        ...
        &lt;/li&gt;
        &lt;/div&gt;
            &lt;/div&gt;
                &lt;/ul&gt;
                    &lt;/li&gt;
                    &lt;a href="..." class="CssFriendly-Menu-Link"&gt;Employees&lt;/a&gt;
class="CssFriendly-Menu-Leaf"&gt;<font style="background-color&#58;rgb(255, 255, 128);">li</font>                    &lt;
class="first"&gt;<font style="background-color&#58;rgb(255, 255, 128);">ul</font>                &lt;
            &lt;div class="CssFriendly-Menu-Dropdown-ItemHost"&gt;
        &lt;div class="cbb CssFriendly-Menu-Dropdown"&gt;
        &lt;a href="..." class="CssFriendly-Menu-Link TopLevelNavItem"&gt;About Us&lt;/a&gt;
class="CssFriendly-Menu-WithChildren"&gt;<font style="background-color&#58;rgb(255, 255, 128);">li</font>        &lt;
class="CssFriendly-Menu"&gt;<font style="background-color&#58;rgb(255, 255, 128);">ul</font>    &lt;
Good example - using CSS Friendly
