---
type: rule
title: Do you use "list" tags for lists only?
uri: do-you-use-list-tags-for-lists-only
created: 2012-07-02T15:02:44.0000000Z
authors:
- id: 16
  title: Tiago Araujo

---

 
​The HTML list tags &lt;ul&gt; and &lt;ol&gt; should be used for unordered and ordered lists **only**.
 
**Tip: **If your list tag (&lt;ul&gt; or &lt;ol&gt;) doesn't have a list item (&lt;li&gt;) inside it, then it's not a list. Consider using another HTML tag (E.g. &lt;p&gt;).

&lt;ul&gt;<br>A normal text<br>&lt;/ul&gt;
Figure: Bad Example - Using the &lt;ul&gt; for a text

&lt;ul&gt;&lt;li&gt;A list item&lt;/li&gt;&lt;/ul&gt;

&lt;ol&gt;&lt;li&gt;A list item&lt;/li&gt;&lt;/ol&gt;

Figure: Good Example - Using the &lt;ul&gt; and &lt;ol&gt; for lists
