---
type: rule
title: HTML/CSS - Do you know how to create spaces in a web page?
uri: htmlcss---do-you-know-how-to-create-spaces-in-a-web-page
created: 2012-07-02T14:19:41.0000000Z
authors:
- id: 16
  title: Tiago Araujo

---

There are many scenarios where you need some extra space in a web page. No matter which one you are at, CSS is the answer.
 
Sometimes the first thing that comes to the developer mind is to use the "break line" tag (&lt;br /&gt;) or the [ASCII character code](http&#58;//en.wikipedia.org/wiki/ASCII) for "space" (&#160;) to create these extra spaces. It's wrong. CSS is the way to go. You can use both "margin" or "padding" CSS properties to get the result you want.

[greyBox] <br>&lt;ul&gt;
<br>&lt;li&gt;&#160;&#160;&#160;List item&lt;/li&gt;
<br>&lt;/ul&gt;
<br> [/greyBox]
Figure: Bad Example - Using the "space" ASCII character to create a padding on that list
[greyBox] <br>&lt;ul&gt;
<br>&lt;li&gt;List item&lt;/li&gt;
<br>&lt;/ul&gt;
<br>&lt;br /&gt;
<br>&lt;br /&gt;
<br>&lt;br /&gt;<br> [/greyBox]
Figure: Bad Example - Using the &lt;br /&gt; tag to create a space at the bottom of that list
[greyBox] <br>ul {margin-bottom:15px;}
<br>ul li {padding-left:10px;}<br> [/greyBox]
Figure: Good Example - Using CSS to add a margin at the bottom of the list a the padding on the left side of each list item
**Tip:**  You might be not familiar with editing a CSS file. In this case, contact a designer. He/She will be more than happy to help you.
