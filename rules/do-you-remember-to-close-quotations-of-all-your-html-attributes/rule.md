---
type: rule
title: Do you remember to close quotations of all your HTML attributes?
uri: do-you-remember-to-close-quotations-of-all-your-html-attributes
created: 2016-08-12T20:46:20.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

It is always better to make sure there are equivalent closing quotations for HTML attributes. A small mistake of missing a quotation could lead to undesired results on the web page.
 
​​

&lt;span style="font-size:12pt; background: #ccc;&gt;
 Figure: Bad code - Can you see the missing quote? Code Auditor can


&lt;span style="font-size:12pt; background: #ccc;"&gt;
Figure: All OK

As you can see from the above example, just missing a quotation makes the whole layout of the text different. So be very careful that you make sure you have closed all opening quotations of attributes with equivalent closing quotations.

We have a program called [SSW Co​de Auditor](https&#58;//www.ssw.com.au/ssw/codeauditor/) to check for this rule. ​
