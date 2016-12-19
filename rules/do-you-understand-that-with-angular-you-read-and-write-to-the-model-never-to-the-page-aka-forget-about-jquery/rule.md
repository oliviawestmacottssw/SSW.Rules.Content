---
type: rule
archivedreason: 
title: Do you understand that with Angular you read and write to the model... never to the page? (a.k.a. Forget about jQuery)
guid: 3cd40e9e-38c3-4558-9a73-65bfb8dc5b6c
uri: do-you-understand-that-with-angular-you-read-and-write-to-the-model-never-to-the-page-aka-forget-about-jquery
created: 2016-04-06T20:18:33.0000000Z
authors:
- title: Adam Stephensen
  url: https://ssw.com.au/people/adam-stephensen
related: []
redirects: []

---


<p>​The most common mistake that developers make when moving from jQuery to Angular is that they continue to think about updating the page.<br></p>
<br><excerpt class='endintro'></excerpt><br>
<dl class="image"><dt> <img src="/PublishingImages/understand-jquery.png" alt="understand-jquery.png" style="width&#58;750px;height&#58;465px;" /></dt><dd>Figure&#58; In jQuery, you design a page and then use jQuery to perform interactions with the page e.g. reading and setting the values of input boxes, updating the content of divs or handling button events</dd></dl><dl class="badImage"><dt><img src="/PublishingImages/understand-badcode.png" alt="understand-badcode.png" /> </dt><dd>Figure&#58; Bad Example - using jQuery on Angular views will lead to worlds of pain</dd></dl><p>A fundamental principal of Angular is that you build a Model in JavaScript (or TypeScript) and then on your view you just databind your UI elements to the model. Any changes that are made are made to the model and the view updates automatically.</p><p><strong>In Angular,&#160;you do&#160;not interact&#160;with the page you update the model, and the page is just displaying a view of the model.</strong></p><dl class="goodImage"><dt><img src="/PublishingImages/understand-goodcode.png" alt="understand-goodcode.png" style="margin&#58;5px;width&#58;750px;height&#58;121px;" /></dt><dd>Figure&#58; Good Example - In both AngularJs &amp; Angular 2.0 jQuery is not required on the view. The view binds to properties on a JavaScript model</dd></dl><p>Further reading&#58;&#160;<a href="http&#58;//stackoverflow.com/questions/14994391/thinking-in-angularjs-if-i-have-a-jquery-background" target="_blank">http&#58;//stackoverflow.com/questions/14994391/thinking-in-angularjs-if-i-have-a-jquery-background </a> </p>


