---
type: rule
archivedreason: 
title: Practices - Do you avoid directly modifying the DOM from your components?
guid: 5537a14f-cc51-48fe-828c-b8abc240070f
uri: practices-do-you-avoid-directly-modifying-the-dom-from-your-components
created: 2016-04-22T22:18:30.0000000Z
authors:
- title: Steve Leigh
  url: https://ssw.com.au/people/steve-leigh
- title: Gabriel George
  url: https://ssw.com.au/people/gabriel-george
related: []
redirects: []

---


<p>​U​sing DOM is fine, but manipulating DOM directly in your component is not. ​With the introduction of Angular, there has been a big push in ensuring the DOM stays out of your JavaScript code.  It is designed in such a way that an existing Angular application can be ported to another target by simply replacing the template and template loader.  Projects such as <a href="http://angularjs.blogspot.com.au/2016/04/angular-2-react-native.html">Angular React Native Renderer</a> leverages this to allow native mobile app development in Angular.​​<br></p>
<br><excerpt class='endintro'></excerpt><br>
<ul><li>Smaller component code making it easier to maintain</li><li>Faster running and easier to write unit tests</li><li>Easier for designers to get involved <br></li></ul><p>This means that the component's state must expose things that are useful to the template as public properties or fields, and the Angular should read these fields to draw itself.</p><dl class="badImage"><dt><img src="dom1.png" alt="dom1.png" /> </dt><dd>This component manipulates the DOM directly to show and hide the menu</dd></dl><dl class="goodImage"><dt><img src="dom2.png" alt="dom2.png" /></dt><dd>This component sets component state, which the template can use.  It is simpler, more descriptive and easier to test</dd></dl>


