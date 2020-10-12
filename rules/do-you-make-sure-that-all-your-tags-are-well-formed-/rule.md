---
type: rule
title: Do you make sure that all your tags are well formed ?
uri: do-you-make-sure-that-all-your-tags-are-well-formed-
created: 2011-04-28T09:29:10.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

Do you know how to form HTML/XML tags on webpages?
<br>We need to make sure that all HTML/XML tags which open once, must be closed properly.<br> 

[[greyBox]]
|  <br>&lt;div&gt;   
| <br>&lt;p&gt;Hello HTML&lt;/p&gt;   
| <br>&lt;/div&gt;<br>
| <br> Figure: Good Example


[[greyBox]]
|  <br>&lt;breakfast\_menu&gt;<br>
| <br>&lt;food&gt;<br>
| <br>&lt;name&gt;Homestyle Breakfast&lt;/name&gt;<br>
| <br>&lt;price&gt;$6.95&lt;/price&gt;<br>
| <br>&lt;description&gt;two eggs&lt;/description&gt;<br>
| <br>&lt;calories&gt;950&lt;/calories&gt;<br>
| <br>&lt;/food&gt;
| <br>&lt;/breakfast\_menu&gt;<br> Figure: Good Example

[[greyBox]]
|  <br>&lt;div&gt;   
| <br>&lt;p&gt;Hello HTML  
| <br>&lt;/div&gt;<br>
| <br> Figure: Bad Example

[[greyBox]]
|  <br>&lt;breakfast\_menu&gt;<br>
| <br>&lt;food&gt;<br>
| <br>&lt;name&gt;Homestyle Breakfast<br>
| <br>&lt;price&gt;$6.95<br>
| <br>&lt;description&gt;two eggs<br>
| <br>&lt;calories&gt;950<br>
| <br>&lt;/food&gt;
| <br>&lt;/breakfast\_menu&gt;<br> Figure: Bad Example
