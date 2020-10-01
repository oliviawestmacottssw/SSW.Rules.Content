---
type: rule
title: Do you use jQuery instead of JavaScript?
uri: do-you-use-jquery-instead-of-javascript
created: 2016-11-17T15:55:05.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

jQuery is the MUST HAVE tool for web developers. There are 3 good reasons why you should use jQuery.

1. Cross Browsers (IE 6.0+, Firefox 2+, Safari 3.0+, Opera 9.0+, Chrome)
2. Powerful and easy to use
    - Same selectos as CSS
    - Designer can learn it fast
    - More readable JavaScript code
3. Plug-ins - Tons of useful plug-ins and functionalities


 
window.onload = function() { alert("Welcome"); }
Figure: Bad Example - Using JavaScript 'onload' event

$(document).ready(function() { alert("Welcome!"); });
Figure: Good Example - using jQuery document 'ready' event
