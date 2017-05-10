---
type: rule
archivedreason: 
title: Do you know the right way to create your Angular project?
guid: bc2dd342-6109-461f-8e9b-cd6b3e5aaa4e
uri: do-you-know-the-right-way-to-create-your-angular-project
created: 2016-10-27T21:33:46.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
- title: Adam Stephensen
  url: https://ssw.com.au/people/adam-stephensen
- title: Brendan Richards
  url: https://ssw.com.au/people/brendan-richards
- title: Jean Thirion
  url: https://ssw.com.au/people/jean-thirion
related: []
redirects: []

---


​<a href="http&#58;//angular.io/" target="_blank">Angular.io​</a> is a great place to get started learning Angular 2, but do not use the tutorials as the template for your real apps!​​<br>
<br><excerpt class='endintro'></excerpt><br>
<p>The <a href="https&#58;//angular.io/docs/ts/latest/quickstart.html" target="_blank">Quick Start </a>&#160;and <a href="https&#58;//angular.io/docs/ts/latest/tutorial/" target="_blank">Tour of Heros Tutorial</a>&#160;will teach you lots about Angular 2 but are not examples of real world projects because&#58;</p><ol><li>They do not include a method to create a production build output<br>See <a href="/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=ac5174c4-a417-4bf8-a3ac-c47bdb8f273c">Do you know the best build tool? </a> <br></li><li>They do not consider whether your application will require the redux pattern&#160;<br>See <a href="/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=e4d1e090-bee8-4a86-9a46-fa46aa7f8058">Do you know to use ngrx on complex applications? </a> <br></li><li>They do not include a UI framework <br>See <a href="/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=1c35f4c4-7f94-4c88-8bbf-a81dfc77f5d7">Do you know the best UI framework for Angular 2? </a> </li></ol><p><br></p><p>There are also several well used templates that incorporate Angular and&#160;server-side tooling.</p><p>The leading example is the ASP.NET template for Angular&#160;<a href="https&#58;//github.com/aspnet/JavaScriptServices/tree/dev/templates" target="_blank">https&#58;//github.com/aspnet/JavaScriptServices/tree/dev/templates</a>.&#160;<br>While these starters&#160;often include advanced functionality, we prefer to implement pure Angular CLI projects where possible because&#160;Angular updates&#160;frequently.. and when you are using someone else's template that incorporates Angular you are left with the options of waiting for them to update their template to the latest version of Angular, or working out how to​ do it yourself. This can often leave you with large amounts of work or be being several months behind the latest versions.<br></p><p>To learn how to build <strong>real-world&#160;Angular 2 applications</strong> check out <a href="http&#58;//firebootcamp.com/angular2">FireBootCamp</a>.<br></p><dl class="badImage"><dt><img src="/PublishingImages/create-angular-bad.png" alt="create-angular-bad.png" /></dt><dd>Figure&#58; Bad Example - Using regular Angular tutorials</dd></dl><dl class="goodImage"><dt><img src="/PublishingImages/create-angular-good.png" alt="create-angular-good.png" /></dt><dd>Figure&#58; Good Example&#58; The Angular CLI will create you a new Angular 2 project with a single command, and that project will be all setup with production build, unit testing and end to end testing all configured. If you have very specific&#160;build requirements the CLI does not currently support custom webpack builds, though this is coming. See&#160;<a href="/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=ac5174c4-a417-4bf8-a3ac-c47bdb8f273c">https&#58;//rules.ssw.com.au/the-best-build-tool</a>&#160;for more info <br></dd></dl>


