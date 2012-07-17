---
type: rule
title: Do you know how to use named anchor links?
uri: do-you-know-how-to-use-named-anchor-links
created: 2012-07-17T20:11:55.0000000Z
authors:
- id: 16
  title: Tiago Araujo

---

 
The attribute "name" allow you to link to specific places within the page via &lt;a&gt; tag.

Suppose you have a long page with different sections. You can create a named anchor in each of these section headings to provide a "jump-to" functionality. In other words, you can have a different URL for each piece of content on the same page.

To do so you should create a empty link tag with the attribute name you prefer:
&lt;h2&gt;&lt;a name="get-started"&gt;&lt;/a&gt;Get Started&lt;/h2&gt;Figure: Code for a named anchor link. Note it doesn't have the hash mark 
To create a link to that section, simply add a hash mark to the end of the URL followed by the name you chose:
&lt;a href="#get-started"&gt;Go to Get Started section&lt;/a&gt;Figure: Code to link to a named section of a page. Remember to add the hash mark

**Tip:** Use the hash mark only to go to the top of thepage.

E.g. &lt;a href="#"&gt;&Go to top&lt;/a&gt;


