---
type: rule
title: Do you use Hyperlinks instead of JavaScript to open pages?
uri: do-you-use-hyperlinks-instead-of-javascript-to-open-pages
created: 2013-07-28T03:04:16.0000000Z
authors:
- id: 23
  title: Damian Brady

---

 If possible you should always use hyperlinks to open new pages on your site instead of using JavaScript.
 
​There are two good reasons for avoiding JavaScript-powered links:

1. Copying and pasting sections of the site to an email or a document will maintain the clickable links
2. There's an (ever-decreasing) chance a user won't have JavaScript enabled and won't be able to click the link



&lt;div onclick="window.open('mynewpage.html');"&gt;Open a new page&lt;/div&gt;​
Figure: Bad Example - This link can't be clicked on if you paste it into an email​ or if JavaScript is off

&lt;a href="mynewpage.html"&gt;Open a new page&lt;/a&gt;
Figure: Good Example - This link can still be clicked on when pasted and when JavaScript is turned off​
