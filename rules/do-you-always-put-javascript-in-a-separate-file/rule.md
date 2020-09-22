---
type: rule
title: Do you always put JavaScript in a separate file?
uri: do-you-always-put-javascript-in-a-separate-file
created: 2016-09-01T18:32:24.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

 ASP.NET injects many lines during page rendering, so if you are using inline JavaScript, the line numbers will change during client side JavaScript debugging in VS.NET, FireBug or IE8 developer Tools.
​​​
 ![JavaScriptBad1.jpg](JavaScriptBad1.jpg)Figure: Bad Code - Using Inline JavaScript![JavaScriptBad.jpg](JavaScriptBad.jpg)Figure: Bad Code - On PostBack Line numbers are changed for Inline JavaScript![JavaScriptGood.jpg](JavaScriptGood.jpg)Figure: Good Code - Using JavaScript on Separate file ​

So you should always put JavaScript in a separate file.  Then the line numbers will stay consistent during debugging. 
Keeping JavaScript in a separate file is also good for production as it improves performance due to browser caching. 

**Note: **During development, remember to hit CTRL-F5 to force the browser to re-fetch the files from the server or you may be debugging old version of the JavaScript file.

