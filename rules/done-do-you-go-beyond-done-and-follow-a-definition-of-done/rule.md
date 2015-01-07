---
type: rule
archivedreason: 
title: Done - Do you go beyond 'Done' and follow a 'Definition of Done'?
guid: f8b61f21-7d1f-497f-a63f-4b9b98c2156c
uri: done-do-you-go-beyond-done-and-follow-a-definition-of-done
created: 2010-02-10T00:09:02.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
- title: Peter Gfader
  url: https://ssw.com.au/people/peter-gfader
- title: Paul Neumeyer
  url: https://ssw.com.au/people/paul-neumeyer
- title: Damian Brady
  url: https://ssw.com.au/people/damian-brady
related: []
redirects: []

---


​Having a clear Definition of Done for&#160;your team is critical to&#160;your success and quality management in Scrum.<br><br>Every team is different, but all need to agree on which items are in their &quot;Definition of Done&quot;. 
<br><excerpt class='endintro'></excerpt><br>
<h1>There are 3 levels of &quot;Done&quot; in communication</h1><h2>Level 1</h2><ul><li>Sending a <a href="/dones-do-you-reply-done-and-delete-the-original-email">&quot;Done&quot; email</a>​</li></ul><h2>Level 2</h2><ul><li>Sending a &quot;Done&quot; email</li><li>screenshots</li><li>code</li></ul><h2>Level 3</h2><ul><li>Sending a &quot;Done&quot; email </li><li>video</li><li>code (showing a full scenario e.g. a user story)​</li></ul><h4>Example of a level 3 &quot;done&quot;</h4><div class="greyBox"><p>Subject&#58; RE&#58; Manad - Coded UI Tests #2</p><p style="margin-left&#58;20px;">&gt; Create a new CodedUI test on your feedback form – search only to test the Telerik</p><p>Done</p>
   <img class="ms-rteCustom-ImageArea" alt="Coded UI Test passes in Visual Studio" src="/PublishingImages/level-3-done.jpg" />
   <span class="ms-rteCustom-FigureNormal">Figure – Coded UI Test passes in Visual Studio</span>
   <p>Jing Video of the test running&#58; 
      <a href="http&#58;//screencast.com/t/ps17fqsV" target="_blank">http&#58;//screencast.com/t/ps17fqsV</a> </p></div>
<span class="ms-rteCustom-FigureGood">Figure&#58; Good example - The &quot;done&quot; shows a full scenario</span>
<h1>There are&#160;8 levels of &quot;Done&quot; in software quality</h1><p>Start with these examples showing typical &quot;Definitions of Done&quot; from beginner teams to more mature teams&#58;</p><h2>Team - Level 1</h2><ul><li>The code compiles </li><li>All tasks are updated and closed </li><li>No high priority defects/bugs are on that user story </li></ul><h2>Team - Level 2</h2><ul><li> 
      <em>All of the above, plus</em> </li><li>All unit tests passed </li><li>Greater than 1% code coverage (not earth shattering, but you need to start somewhere)</li></ul><h2>Team - Level 3</h2><ul><li> 
      <em>All of the above, plus</em> </li><li>Successful build on the Build Server </li><li>Check in Policy - Changeset Comments Policy (all checkins must have a comment) </li><li>Check in Policy - Work Items (all checkins must be associated with a work item) </li><li>Code reviewed by one other team member (e.g. Checked by Bill) </li><li>Sending a Done email with screenshots </li></ul>
<img class="ms-rteCustom-ImageArea" alt="Check in policy" src="/PublishingImages/CheckinPolicy.jpg" />
<font class="ms-rteCustom-FigureGood" size="+0">Figure&#58; Good example&#160;- Add check in policies to enforce your Definition of Done</font>
<h2>Team - Level 4</h2><ul><li> 
      <em>All of the above, plus</em> </li><li>All acceptance criteria have been met </li><li>All acceptance criteria have an associated test passing (aka. Automated functional testing with Web Tests (Selenium), Coded UI Tests, or Telerik Tests) </li><li>Sending a Done email (with video recording using Jing) </li></ul>
<img class="ms-rteCustom-ImageArea" alt="Acceptance Tests in MTM" src="/PublishingImages/AcceptanceTestsInMTM.jpg" />
<font class="ms-rteCustom-FigureGood" size="+0">Figure&#58; Good example - Acceptance Tests in MTM</font>
<h2>Team - Level 5</h2><ul><li> 
      <em>All of the above, plus</em> </li><li>Deployed to UAT (ideally using Continuous Deployment) </li><li>Complex code is documented (removing technical debt) </li><li>Product Owner acceptance </li></ul><h2>Team - Level 6</h2><ul><li> 
      <em>All of the above, plus</em> </li><li>Multiple environments automatically tested using Lab Management </li></ul>
<img class="ms-rteCustom-ImageArea" alt="Lab management" src="/PublishingImages/LabManagement.jpg" />
<font class="ms-rteCustom-FigureGood" size="+0">Figure&#58; Good example - A tester Lab Management to create VMs for testing the application, then defines a test plan for that application with Test Case Management</font>
<h2>Team - Level 7</h2><ul><li> 
      <em>All of the above, plus</em> </li><li>Automated Load Testing </li><li>Continuous Deployment </li></ul>
<img class="ms-rteCustom-ImageArea" alt="Acceptance Tests in MTM" src="/PublishingImages/LoadTesting.jpg" />
<font class="ms-rteCustom-FigureGood" size="+0">Figure&#58; Good example - Load testing involves multiple test agents running Web Performance Tests and pounding the application (simulating the behaviour of many simultaneous users)</font><strong>Team - Level 8 (Gold)</strong> 
<ul><li> 
      <em>All of the above, plus</em></li><li>Deployed to Production</li></ul><ul> 
   <span>Congratulations! You are frequently deploying to production. This is called “Continuous Delivery” and allows you to gather quick feedback from your end users.</span> 
   <div style="margin&#58;0cm 0cm 0pt;"> 
      <span style="font-family&#58;verdana, sans-serif;font-size&#58;10pt;"></span>&#160;</div><div style="margin&#58;0cm 0cm 0pt;"> 
      <span style="font-family&#58;verdana, sans-serif;font-size&#58;10pt;"> 
         <em>You might have everything deployed to production, but it might not yet be visible to the end user. This can be achieved by having “</em><a href="http&#58;//martinfowler.com/bliki/FeatureToggle.html"><em>Feature toggles</em></a> <em>”&#160;in place. The actual release of the functionality is a decision that the Product Owner and business takes.</em></span></div>
   <font face="Calibri"> 
      <i></i></font></ul><p> 
   <strong>More Information&#58;​</strong></p><ul><li><a href="/do-your-user-stories-include-acceptance-criteria-(aka-never-assume-automatic-gold-plating)">Do your user stories include acceptance criteria?</a></li><li><a title="Do you enforce comments with check-ins?" href="http&#58;//www.ssw.com.au/ssw/Standards/Rules/RulesToBetterSourceControlwithTFS.aspx#EnforceComments" target="_blank">Do you enforce comments with check-ins?</a> </li><li><a title="Do you enforce work item association with check-in?" href="http&#58;//www.ssw.com.au/ssw/Standards/Rules/RulesToBetterSourceControlwithTFS.aspx#EnforceWorkItemAss" target="_blank">Do you enforce work item association with check-in?</a> </li><li><a title="Do you follow a Test Driven Process?" href="http&#58;//www.ssw.com.au/ssw/Standards/Rules/RulesToBetterVersionControlwithTFS%28AKASourceControl%29.aspx#TestDrivenProcess" target="_blank" shape="rect">Do you follow a Test Driven Process?</a> </li><li></li><li><a href="/do-you-have-a-＂definition-of-ready＂">Do you have a &quot;Definition of Ready&quot;?</a></li></ul>
 


