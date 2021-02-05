---
type: rule
archivedreason: 
title: Printing - Do you have a print.css file so your web pages are nicely printable?
guid: 80e333f6-7200-4b01-b2d4-79d6ced9f4bb
uri: printing-do-you-have-a-print-css-file-so-your-web-pages-are-nicely-printable
created: 2014-12-09T19:14:24.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
- title: Tiago Araujo
  url: https://ssw.com.au/people/tiago-araujo
related: []
redirects: []

---


<p>As we know portable devices like tablets and mobile phones are being more and more used as reading devices, however printing web pages is still often necessary. In general web designers don't think about printing when putting a web site up, meaning we're left with web pages that frustratingly don't properly print on to paper.</p>
<br><excerpt class='endintro'></excerpt><br>
<p>​​A print.css file works in the same way as a regular stylesheet, except it only gets called up when the page is printed, by setting the command media to be &quot;print&quot;, as per below&#58;</p> 
<div><p class="ssw15-rteElement-CodeArea">&lt;link rel=&quot;stylesheet&quot; href=&quot;print.css&quot; type=&quot;text/css&quot; media=&quot;print&quot; /&gt;&#160;​</p></div>

The print.css file should have 100% width and is used to hide elements that you don't want to appear when printing a web page, such as advertising, background, menus, animations etc.


