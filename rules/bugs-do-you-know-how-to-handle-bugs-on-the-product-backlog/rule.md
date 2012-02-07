---
type: rule
archivedreason: 
title: Bugs - Do you know how to handle Bugs on the Product Backlog?
guid: 1e02b1e3-70e2-4aac-a716-c20638ad6424
uri: bugs-do-you-know-how-to-handle-bugs-on-the-product-backlog
created: 2010-05-06T04:38:50.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
- title: Martin Hinshelwood
  url: https://ssw.com.au/people/martin-hinshelwood
- title: Eric Phan
  url: https://ssw.com.au/people/eric-phan
related: []
redirects: []

---



  <p>Story Points cannot be allocated against bugs in MSF Agile 5.0 so to include them in a Sprint we need to group them.
</p>

<br><excerpt class='endintro'></excerpt><br>

  <p>Bugs that are introduced and found because of the current work in the Sprint are included in the Sprint and estimated immediately so the burndown remains accurate.</p>
<p>See <a href="/Pages/CreateBugs.aspx" shape="rect"><font color="#000080">Do you know when to create bugs?</font></a> for detailed information on identifying when something is a bug, and when to just fix it.</p>
<ol>
    <li>
    <h2>Using MSF Agile 5.0</h2>
    <p>Bugs found that are independent of the work on the current Sprint are placed on the Product Backlog as a work item “Bug”. The product Owner then ranks the Bugs with priority amongst the User Stories. Bugs cannot have Story Points allocated to them so User Stories need to be created with Bugs as Child Work Items. This is only done when the PO has prioritized the Bug and the Bug is likely to make the next Sprint. At the Planning Meeting, the PO elects which Bugs are to be included and new User Stories are created to group them appropriately with due regard to Severity and Stack Rank. Once the User Stories have been created, The Team estimates the Story Points for each one; the Product confirms User Stack Rank and the Sprint Backlog is planned as normal.</p>
    <p>This process&#58; </p>
    <ul>
        <li>Works around the problem of Bugs not having Story Points </li>
        <li>Allows Bugs of the same rank to be sensibly grouped together </li>
        <li>Prevents arbitrary groupings of Bugs which cannot be properly ranked </li>
        <li>Follows the estimate just-in-time philosophy of Scrum </li>
        <li>Prevents small Bugs taking up a whole Story Point </li>
    </ul>
    </li>
    <li>
    <h2>Using Visual Studio Scrum 1.0</h2>
    <p>In the Visual Studio Scrum template bugs are just another PBI and you can assign a business priority and an effort estimate in Story Points. Bugs that make the cut for the next sprint can be broken down into tasks and estimated as required.</p>
<p>As bugs from previous sprints are just PBI’s, the PO agrees to a list of bugs that will be fixed in the current Sprint.</p>
<p>The team just fixes any <strong>newly</strong> bugs they introduced in the current sprint.</p>
<p>If the team finds bugs due to functionality accepted in a previous sprint they log it as a PBI and will complete the fix in a future sprint, unless it is a critical bug, in which case they raise it as an impediment to the current sprint to the PO.</p>

<p>Examples&#58;</p>
<ul>
    <li><strong>Small bug</strong> – Text on a label is spelled incorrectly </li>
    <li><strong>Big bug</strong> - There is an error thrown when transitioning from page 1 to page 2 when you hold down the Ctrl key</li>
</ul></li>
<li>
<div><h2 style="line-height&#58;21px;">​​​​​​​Using TFS Preview (TFS 2012)</h2></div>
<p>Bugs found that are independent of the work on the current Sprint are placed on the Product Backlog as a work item “Bug”. The product Owner then ranks the Bugs with priority amongst the User Stories. Bugs can have a value associated with them for effort the same as PBI's. At the Planning Meeting, the PO elects which Bugs are to be included by ordering them on the Product Backlog.</p>
<p>Bugs found within the current Sprint added to the tasks they are related to as child items. The Development Team aims to fix the bug as soon as possible within the current Sprint.</p>
<p><img src="/PublishingImages/tfs_preview_add_bug.png" alt="tfs_preview_add_bug.png" style="margin-top&#58;5px;margin-right&#58;5px;margin-bottom&#58;5px;margin-left&#58;5px;" /><br><br><strong>Figure&#58; Bugs can be added &quot;out of Sprint&quot; directly into the Product Backlog in TFS Preview (TFS 2012)</strong></p></li>
<p>​</p></ol>
​​​​​​​​


