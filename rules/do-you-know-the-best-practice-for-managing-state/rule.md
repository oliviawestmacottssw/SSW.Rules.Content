---
type: rule
archivedreason: 
title: Do you know the best practice for managing state?
guid: ca46ad62-e44e-4266-a68b-e8d1b04e3b08
uri: do-you-know-the-best-practice-for-managing-state
created: 2017-08-15T23:35:06.0000000Z
authors:
- title: Adam Stephensen
  url: https://ssw.com.au/people/adam-stephensen
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
related: []
redirects: []

---


<p>​State management is complex and time-consuming.​​​<br></p>
<br><excerpt class='endintro'></excerpt><br>
<p>The redux pattern helps resolve this issue.<br></p><dl class="badImage"><dt><img src="/PublishingImages/maintaining-state.png" alt="maintaining-state.png" /><br></dt><dd>Bad example&#58; maintaining state on individual components</dd></dl><dl class="goodImage"><dt><img src="/PublishingImages/redux-logo.png" alt="redux-logo.png" /> <br></dt><dd> Good example&#58; use the redux pattern</dd></dl><p>The 4 principles of the redux pattern&#58;<br></p><ol><li>The entire state of the application is represented in a single JavaScript object called a store.<br></li><li>The store is acted upon using special functions called reducers.<br></li><li>State is immutable and reducers are the only part of the application that can change state.<br></li><li>Reducers are pure JavaScript functions. This means they cannot import external dependencies.<br><br></li></ol><div><font color="#333333">Side Effects<br></font></div><div><font color="#333333">To perform operations that require external dependencies (such as communicating with a web server), we can implement side effects. These can use external dependencies but they cannot directly modify the store. They can invoke reducers to modify the store when the side effect is complete</font></div><div><font color="#333333"><br>redux-saga&#160;is a library that provides redux application side effects.<br>The&#160;advantages of using redux-saga are&#58;<br><ol><li>Collects all asynchronous&#160;operations in one place, making the code clearer.<br></li><li>Uses an&#160; ES6 feature called Generators to make asynchronous flows easy to read, write and test.<br></li><li>Generators also let these asynchronous flows look like your standard synchronous code (kind of like&#160;async/await in C#). This&#160;solves “callback hell” [<a href="https&#58;//en.wiktionary.org/wiki/callback_hell">https&#58;//en.wiktionary.org/wiki/callback_hell​</a>]<br></li></ol></font></div><div><font color="#333333"></font></div>


