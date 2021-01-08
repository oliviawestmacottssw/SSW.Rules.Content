---
type: rule
archivedreason: 
title: Do you always put JavaScript in a separate file?
guid: 1d6f7924-8e0a-4dfa-b8dc-d3960cfcd3b7
uri: do-you-always-put-javascript-in-a-separate-file
created: 2016-09-01T18:32:24.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
related: []
redirects:
- always-put-javascript-in-a-separate-file

---

ASP.NET injects many lines during page rendering, so if you are using inline JavaScript, the line numbers will change during client side JavaScript debugging in VS.NET, FireBug or IE8 developer Tools.


<!--endintro-->
<dl class="badImage"><dt><img src="JavaScriptBad1.jpg" alt="JavaScriptBad1.jpg"></dt><dd>Figure: Bad Code - Using Inline JavaScript</dd></dl><dl class="badImage"><dt><img src="JavaScriptBad.jpg" alt="JavaScriptBad.jpg"></dt><dd>Figure: Bad Code - On PostBack Line numbers are changed for Inline JavaScript</dd></dl><dl class="goodImage"><dt><img src="JavaScriptGood.jpg" alt="JavaScriptGood.jpg"></dt><dd>Figure: Good Code - Using JavaScript on Separate file <br></dd></dl>
So you should always put JavaScript in a separate file.  Then the line numbers will stay consistent during debugging. 
Keeping JavaScript in a separate file is also good for production as it improves performance due to browser caching. 

 **Note:** During development, remember to hit CTRL-F5 to force the browser to re-fetch the files from the server or you may be debugging old version of the JavaScript file.
