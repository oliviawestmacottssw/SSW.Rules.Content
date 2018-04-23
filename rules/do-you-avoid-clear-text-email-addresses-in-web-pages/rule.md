---
type: rule
archivedreason: 
title: Do you avoid clear text email addresses in web pages?
guid: ab0fc8a3-97b0-43ac-b944-9ac6ef9a65a8
uri: do-you-avoid-clear-text-email-addresses-in-web-pages
created: 2018-04-23T20:39:13.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
related: []
redirects: []

---


<p>Clear text email addresses in web pages are very dangerous because it gives spam sender a chance to pick up your email address, which produces a lot of spam/traffic to your mail server, this will cost you money and time to fix.<br></p><p>Never put clear text email address on web pages.<br></p>
<br><excerpt class='endintro'></excerpt><br>
<p class="ssw15-rteElement-CodeArea" style="width&#58;770.031px;">&lt;!--SSW Code Auditor - Ignore next line(HTML)--&gt;&#160;<br>&lt;a href=&quot;mailto&#58;test@ssw.com.au&quot;&gt;Contact Us&lt;/a&gt;</p><dd class="ssw15-rteElement-FigureBad">Bad - Using a plain email address that it will be crawled and made use of easily​<br></dd><p class="ssw15-rteElement-CodeArea" style="width&#58;770.031px;">​&lt;a href=&quot;javascript&#58;sendEmail('74657374407373772e636f6d2e6175')&quot;&#160;onmouseover=&quot;javascript&#58;displayStatus('74657374407373772e636f6d2e6175');return true;&quot;&#160;onmouseout=&quot;javascript&#58;clearStatus(); return true;&quot;&gt;Contact Us&lt;/a&gt;<br></p><dd class="ssw15-rteElement-FigureGood">Good - Using an encoded email address​​<br></dd><p><strong><br></strong></p><p><strong>Note&#58;</strong>&#160;If you use Wordpress, use the&#160;<a href="http&#58;//wordpress.org/extend/plugins/email-encoder-bundle">Email Encoder Bundle plugin</a>&#160;to help you encode email addresses easily.</p><p class="ssw15-rteElement-YellowBorderBox">We have a program called&#160;<a href="https&#58;//www.ssw.com.au/ssw/CodeAuditor/">SSW CodeAuditor</a>&#160;to check for this rule.​<br>We have a program called&#160;<a href="https&#58;//www.ssw.com.au/ssw/LinkAuditor/">SSW Link​Auditor</a>&#160;to check for this rule.​​​<br></p>


