---
type: rule
archivedreason: 
title: Do you use Exploratory Testing to create Acceptance Tests?
guid: fb39e79c-8749-4467-9327-518a768b0495
uri: do-you-use-exploratory-testing-to-create-acceptance-tests
created: 2013-08-07T22:15:34.0000000Z
authors:
- title: Damian Brady
  url: https://ssw.com.au/people/damian-brady
related: []
redirects: []

---


In an agile team, pre-planning all your tests is not always the most efficient use of time for testers. &#160;PBIs can change direction, scope, and priority, and pre-planned tests are likely to change.<div><br></div><div>Exploratory testing provides the best&#160;way&#160;to create repeatable tests from the acceptance criteria - as you need them.​</div>
<br><excerpt class='endintro'></excerpt><br>
There are two ways to run an exploratory test in Microsoft Test Manager.<div><br></div><div><img src="/PublishingImages/exploratory_2.png" alt="exploratory_2.png" style="margin&#58;5px;width&#58;650px;" /><br></div><dd class="ssw15-rteElement-FigureBad">Figure&#58; Bad Example - go to the Test tab, choose Do Exploratory Testing, choose a PBI, then click Explore. Too many steps.</dd><div><br></div><div><img src="/PublishingImages/exploratory_1.png" alt="exploratory_1.png" style="margin&#58;5px;" /><br></div><dd class="ssw15-rteElement-FigureGood">Figure&#58; Good Example - Right-click on a requirement in your test suite&#160;and choose Explore requirement</dd><div><strong>Note&#58; </strong>You should always run an exploratory test against a PBI. This will automatically relate any&#160;bugs and test cases to that&#160;PBI (not to mention&#160;the exploratory test run).</div><div><br></div><div>When you start&#160;an Exploratory test, you don't see any test steps, but you can click on the title of the requirement to see its Acceptance Criteria.</div><div><br></div><div><img src="/PublishingImages/show_criteria.png" alt="show_criteria.png" style="margin&#58;5px;" /><br></div><dd class="ssw15-rteElement-FigureNormal">Figure&#58; Clicking on the title will show you the Acceptance Criteria</dd><div><strong>Note&#58;</strong> <a href="/Pages/Do-Your-User-Stories-Include-Acceptance-Criteria.aspx">You should always have Acceptance Criteria on your PBIs!</a></div><div><br></div><div>If you find a bug while testing, click the <strong>Create bug</strong> button to add a bug related to the PBI.</div><div><br></div><div><img src="/PublishingImages/create_bug.png" alt="create_bug.png" style="margin&#58;5px;" /><br></div><dd class="ssw15-rteElement-FigureNormal">Figure&#58; Creating a bug from an exploratory test links to the PBI</dd><p class="ssw15-rteElement-P">By default, the reproduction steps will be populated with the last 10 actions you took (you can <a href="http&#58;//geekswithblogs.net/TarunArora/archive/2011/12/14/mtm-11-configuration-settings-amp-customization.aspx">change this and other&#160;defaults&#160;with&#160;configuration</a>)​. &#160;You can cut this down to just&#160;the relevant&#160;actions by clicking Change steps.</p><div><img src="/PublishingImages/change_bug_steps.png" alt="change_bug_steps.png" style="margin&#58;5px;" /><br></div><dd class="ssw15-rteElement-FigureNormal">Figure&#58; You can change the repro steps captured in the bug very easily</dd><div>Now you have a bug, you should create a matching test case so you can verify when the bug is fixed. &#160;This also gives you a handy regression test to help ensure the problem isn't reproduced later.</div><div><br></div><div><img src="/PublishingImages/save_create_test.png" alt="save_create_test.png" style="margin&#58;5px;" /><br></div><dd class="ssw15-rteElement-FigureNormal">Figure&#58; Click Save and create test to create a matching test case</dd><div>Again, the steps are prepopulated from your bug steps.</div><div><br></div><div><img src="/PublishingImages/create_test.png" alt="create_test.png" style="margin&#58;5px;" /><br></div><dd class="ssw15-rteElement-FigureNormal">Figure&#58; The test steps are prepopulated from the action recording</dd><div><br></div>


