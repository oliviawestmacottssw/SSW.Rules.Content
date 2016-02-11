---
type: rule
archivedreason: 
title: Do you know the 3 steps to completing a PBI?
guid: 1de9df77-9b69-4242-b648-e08e5980e9a6
uri: do-you-know-the-3-steps-to-completing-a-pbi
created: 2013-08-30T06:33:21.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
- title: Eric Phan
  url: https://ssw.com.au/people/eric-phan
related: []
redirects: []

---


​​​The lifecycle of a PBI can be broken down into 3 steps&#58;
<br><excerpt class='endintro'></excerpt><br>
<h3>1. Ready</h3><ol><li>Take the next PBI that was created by the Product Owner</li><li>Is the PBI ready?<br>Check your PBI against your Definition of Ready. “Ready” PBIs must have Acceptance Criteria. A good Definition of Ready also encourages a test first mentality in requirements e.g. Use Spec Flow (Given, When, Then) and/or create Test Cases and Test Steps first.</li><li>Break down your PBI into tasks.</li><li>Don't forget to make a task for testing! (So that it is visible in the task board).</li></ol><dl class="image"><dt> <img src="/PublishingImages/Testing%20task.png" alt="Testing task.png" style="width&#58;600px;" /> </dt><dd>Figure&#58; Testing Task added to PBI</dd></dl><h3>2. Code</h3><ol><li>Create a branch for your PBI</li><li>On the Web Task Board, move your Task into “In Progress”</li><li>Code, code, commit… Code, code, commit (Red Green Refactor)</li><li>As you complete tasks, move them to “Done”</li><li>Repeat 2-4</li><li>If you want feedback early, record a video. E.g. Snagit<br></li></ol><h3>3. Done</h3><p>Is the PBI “Done”? Check your Definition of Done, and then the Tester&#58;</p><ol><li>Open a pull request</li><li>Do an &quot;over the shoulder&quot; check of the code</li><li>Use&#160;<a href="/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=14be0d02-79ad-4286-8b78-4f28b0ed4eea">Microsoft's &quot;Exploratory Tester&quot; Chrome extension </a>&#160;to test the app&#160;</li><li>Make changes based on feedback (and then get more feedback)</li><li>Merge changes to master, this automatically deploys (to either Test, Staging or Prod based on process maturity)</li><li>Send a &quot;done&quot; email</li>

</ol>​<span style="line-height&#58;1.6;">Congrats. Your PBI is now ready to be demonstrated during your Sprint Review! (Note&#58; This is also the same process you follow for a Bug work&#160;item)</span><dl class="goodImage"><dt> <a href="/PublishingImages/livecycle.jpg"></a> <img src="/PublishingImages/3StepsToAPBI.jpg" alt="3StepsToAPBI.jpg" style="width&#58;590px;" /> </dt><dd>Good Figure&#58; This image includes all the important steps in a PBI lifecycle. Print this &quot;<a href="/Documents/3StepsToAPBI.pdf">SSW 3 Steps to a PBI pdf</a>&quot; and put it on your 'War Room' wall.</dd></dl>


