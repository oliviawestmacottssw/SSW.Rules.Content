---
type: rule
title: Do you know how to use named anchor links?
uri: do-you-know-how-to-use-named-anchor-links
created: 2012-07-17T20:11:55.0000000Z
authors:
- id: 16
  title: Tiago Araujo

---

 
The attribute "name" allows you to link to specific places within the page, via the &lt;a&gt; tag.

This is especially useful in long pages that can be separated into sections. You can create a named anchor in each of these section headings to provide "jump-to" functionality. In other words, you can have a different URL for each piece of content on the same page.
  &lt;h2&gt;&lt;a name="get-started"&gt;&lt;/a&gt;Get Started&lt;/h2&gt; Figure: Good example - This is how you add an anchor name to an specific section of your page. Note it doesn't have the hash mark
To create a link to that section, simply add a hash mark to the end of the URL followed by the name you chose:
 &lt;a href="#get-started"&gt;Go to Get Started section&lt;/a&gt; Figure: Good example - This is how you add a \*link\* to that anchor name you created. Remember to add the hash mark
**Tip #1:** Use the hash mark **only** to go to the top of a page. 
E.g. &lt;a href="#"&gt;&Go to top&lt;/a&gt;

**Tip #2:** Some browsers consider capitalization for anchor names (E.g. Firefox). Always check your links and anchor names are identical, matching the capitalization.

