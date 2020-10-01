---
type: rule
title: Do you use the .ready() function?
uri: do-you-use-the-ready-function
created: 2013-04-29T06:39:55.0000000Z
authors:
- id: 23
  title: Damian Brady

---

Putting your initialization JavaScript code inside the .ready function is not always required, but it's much safer to do so. 
jQuery exposes a [.ready event](http&#58;//api.jquery.com/ready/) which fires when the Document Object Model (DOM) is fully loaded and ready to be manipulated.

You can attach a function to this event so you can be sure the page is ready for you to work on.

$('#login').addClass('hidden');

Figure: Bad Example - if this jQuery is in the wrong place, the #login element may not exist!

$(function() {
    $('#login').addClass('hidden');
});

Figure: Good Example - this code won't run until the DOM is fully loaded
