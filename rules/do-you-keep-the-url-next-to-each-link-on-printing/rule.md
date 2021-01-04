---
type: rule
archivedreason: 
title: Do you keep the URL next to each link on printing?
guid: b91ec62e-beea-42b3-8d70-6349dd1fc889
uri: do-you-keep-the-url-next-to-each-link-on-printing
created: 2016-06-08T21:04:47.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
- title: Tiago Araujo
  url: https://ssw.com.au/people/tiago-araujo
related: []
redirects: []

---


​​We have a rule on <a href="/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&TermId=f19d44f5-5c5b-4cc8-905d-3f7ddb1edf58">using relevant words on links </a>. How to make sure people will know which words are links and what the links are after printing a page?<br>
<br><excerpt class='endintro'></excerpt><br>
<p>As a good practice, you should use CSS to print the URL's next to each link when printing:</p><p class="ssw15-rteElement-CodeArea">@media print {<br>a[href]:after {<br>content: " (" attr(href) ")";<br>}<br>}</p>​<span style="line-height:1.5em;">In specific cases, like on breadcrumbs and logo, you don't want these URL's, so you should override the style:</span>
<div><p class="ssw15-rteElement-CodeArea">@media print {<br><span class="ssw15-rteStyle-Highlight">.breadcrumb </span>a[href]:after {<br>content: <span class="ssw15-rteStyle-Highlight">none</span>;<br>}</p>
​
   <dl class="goodImage"><dt><img src="print-url.jpg" alt="print-url.jpg" /> </dt><dd>Figure: Good example - printing links on the content but avoiding it on obvious places, like the logo and bradcrumbs</dd></dl></div>


