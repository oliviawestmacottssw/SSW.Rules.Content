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

It is extremely important to make your site standards compliant:

- It makes styling a lot easier.
- It also means your site is likely to work for all browsers, even if you don’t specifically target/support them.
- It requires accessibility for big public sites can be met easier.


When you first run your SharePoint site – you’ll discover that it looks nice on the surface but needs a significant amount of work to fix all the bad HTML.

Implement CSS Friendly – these are the control adapters released by Microsoft to make ASP.NET render better, non-table based controls.  You can implement them for SharePoint sites as well.
&lt;TABLE id=zz1\_TopNavigationMenu class="..." border=0 cellSpacing=0 cellPadding=0&gt;
<br>            &lt;TBODY&gt;
<br>                &lt;TR&gt;
<br>                &lt;TD id=zz1\_TopNavigationMenun0&gt;
<br>                    &lt;TABLE class="..." border=0 cellSpacing=0 cellPadding=0 width="100%"&gt;
<br>                    &lt;TBODY&gt;
<br>                        &lt;TR&gt;
<br>                            &lt;TD style="WHITE-SPACE: nowrap"&gt;
<br>                            &lt;A style="..." class="..." href="..."&gt;Home&lt;/A&gt;
<br>                            &lt;/TD&gt;
<br>                        &lt;/TR&gt;
<br>                    &lt;/TBODY&gt;
<br>                    &lt;/TABLE&gt;
<br>                &lt;/TD&gt;
<br>                ...   
<br>                &lt;TD id=zz1\_TopNavigationMenun1&gt;
<br>                    &lt;TABLE class="..." border=0 cellSpacing=0 cellPadding=0 width="100%"&gt;
<br>                    &lt;TBODY&gt;
<br>                        &lt;TR&gt;
<br>                            &lt;TD style="WHITE-SPACE: nowrap"&gt;
<br>                            &lt;A style="..." class="..." href="..."&gt;Operations&lt;/A&gt;
<br>                            &lt;/TD&gt;
<br>                        &lt;/TR&gt;
<br>                    &lt;/TBODY&gt;
<br>                    &lt;/TABLE&gt;
<br>                &lt;/TD&gt;
<br>                ...
<br>                &lt;TD id=zz1\_TopNavigationMenun2&gt;
<br>                    &lt;TABLE class="..." border=0 cellSpacing=0 cellPadding=0 width="100%"&gt;
<br>                    &lt;TBODY&gt;
<br>                        &lt;TR&gt;
<br>                            &lt;TD style="WHITE-SPACE: nowrap"&gt;
<br>                            &lt;A style="..." class="..." href="..."&gt;Application Management&lt;/A&gt;
<br>                            &lt;/TD&gt;
<br>                        &lt;/TR&gt;
<br>                    &lt;/TBODY&gt;
<br>                    &lt;/TABLE&gt;
<br>                &lt;/TD&gt;
<br>                ...
<br>                &lt;/TR&gt;
<br>            &lt;/TBODY&gt;
<br>            &lt;/TABLE&gt;Bad example - without using CSS Friendly &lt;div class="CssFriendly-Menu-Horizontal" id="zz1\_TopNavigationMenu"&gt;
<br>        &lt;ul class="CssFriendly-Menu"&gt;
<br>            &lt;li class="CssFriendly-Menu-WithChildren"&gt;
<br>            &lt;a href="..." class="CssFriendly-Menu-Link TopLevelNavItem"&gt;About Us&lt;/a&gt;
<br>            &lt;div class="cbb CssFriendly-Menu-Dropdown"&gt;
<br>                &lt;div class="CssFriendly-Menu-Dropdown-ItemHost"&gt;
<br>                    &lt;ul class="first"&gt;
<br>                        &lt;li class="CssFriendly-Menu-Leaf"&gt;
<br>                        &lt;a href="..." class="CssFriendly-Menu-Link"&gt;Employees&lt;/a&gt;
<br>                        &lt;/li&gt;
<br>                    &lt;/ul&gt;
<br>                &lt;/div&gt;
<br>            &lt;/div&gt;
<br>            &lt;/li&gt;
<br>            ...
<br>        &lt;/ul&gt;
<br>    &lt;/div&gt; Good example - using CSS Friendly
