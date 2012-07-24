---
type: rule
archivedreason: 
title: Do you separate JavaScript functionality (AKA Unobtrusive JavaScript)?
guid: f1b16439-54da-4f6f-85a8-c86aff65484e
uri: do-you-separate-javascript-functionality-aka-unobtrusive-javascript
created: 2012-07-24T18:09:29.0000000Z
authors:
- title: Tiago Araujo
  url: https://ssw.com.au/people/tiago-araujo
related: []
redirects: []

---


<p>A website can be broken down into three main development parts&#58; content, design and functionality. To optimize a website for search engines, it's important to separate the content&#160; (crucial for search engines) from design and functionality (not important for SEO).</p>
<br><excerpt class='endintro'></excerpt><br>
<p>All JavaScript code should go into an external .js file (linked to the document with a &lt;script&gt; tag in the head of the page) and not embedded within HTML. The same should be done for CSS files. Don't bloat your HTML file and confuse search engines. Separate the legitimate content from what is programming code.</p>

<div class="ms-rteCustom-CodeArea">
<p>&lt;a onclick=&quot;action()&quot; href=&quot;#&quot;&gt;Click Here&lt;/a&gt;</p>
</div>
<span class="ms-rteCustom-FigureBad">Figure&#58; Never include Javascript as inline attributes</span>
<div class="ms-rteCustom-CodeArea">
<p>&lt;a href=&quot;backuplink.html&quot; class=&quot;action&quot;&gt;Click Here&lt;/a&gt;</p>
</div>
<span class="ms-rteCustom-FigureGood">Figure&#58; Javascript (included in an external file) should use a class or id for its behaviours</span>


