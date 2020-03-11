---
type: rule
archivedreason: 
title: Do you reference the issue ID when writing a test to confirm a bugfix?
guid: 71a28a7c-3f3f-4cea-b0e4-4f1a5dc58f76
uri: do-you-reference-the-issue-id-when-writing-a-test-to-confirm-a-bugfix
created: 2020-03-11T20:48:03.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
related: []
redirects: []

---


When you are adding a unit test for Email validation it is easy to come up with obvious names eg. &quot;TestValidEmails()&quot; and &quot;TestInvalidEmails()&quot;.<br>But when you have just read a bug report and there are 5 steps to reproduce it, people come up with all sorts of long wacky names to explain the 5 steps.<br>
<br><excerpt class='endintro'></excerpt><br>
<p class="ssw15-rteElement-CodeArea">​TestEnterTitleSaveGoBackResave</p><dd class="ssw15-rteElement-FigureBad">Figure&#58; Bad example - The test name reads like repro steps.​​​​<br></dd><p class="ssw15-rteElement-CodeArea">TestProj11</p><dd class="ssw15-rteElement-FigureGood">Figure&#58; Good example - The test is the issue name and you can understand by visiting the issue in your bug database​​<br></dd><p class="ssw15-rteElement-CodeArea"> ///<br> Test case where a user can cause an application exception on the<br> Seminars webpage<br> 1. User enters a title for the seminar<br> 2. Saves the item<br> 3. Presses the back button<br> 4. Chooses to resave the item<br> See&#58; https&#58;//server/jira/browse/PROJ-11<br> ///<br>[Test]<br>public void TestProj11()<br>&#123;<br>&#125;</p><dd class="ssw15-rteElement-FigureGood">Figure&#58; Good comments for the unit test​​​<br></dd>


