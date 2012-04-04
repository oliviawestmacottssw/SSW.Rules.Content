---
type: rule
archivedreason: 
title: Do you review the code comments?
guid: 4a1ae65e-893e-44cd-a37b-9b914909b291
uri: do-you-review-the-code-comments
created: 2012-04-01T09:31:34.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
- title: Damian Brady
  url: https://ssw.com.au/people/damian-brady
related: []
redirects: []

---


<p>Comments can be useful for documenting code, but should be used properly. Some developers like seeing lots of code comments, and some don't.</p>
<br><excerpt class='endintro'></excerpt><br>
<p><span lang="EN-AU"></span>Some tips for including comments in your code are&#58;</p>
<ol><li><span><span lang="EN-AU">Comments aren't aways the solution.&#160; Sometimes it's better to refactor the comments into the actual method name. If your method needs a comment to tell a developer what it does, then the method name is probably not very clear.</span></span></li>
<li><span><span lang="EN-AU">Comments should never say <strong>*what*</strong> the code does, it should say <strong>*why*</strong> the code does it.&#160; Any decent developer can work out what a piece of code does.</span></span></li>
<li><span><span lang="EN-AU">Comments can also be useful when code is missing.&#160; For example, why there is no locking code around a thread-unsafe method.</span></span></li></ol>
<p><span class="ssw-rteStyle-CodeArea"><span style="background-color&#58;#ffff00;">// returns the Id of the first customer with the matching last name</span><br>public int GetResult(string lastname)<br>&#123;<br>&#160;&#160;&#160; <span style="background-color&#58;#ffff00;">// get the first matching customer from the repository</span><br>&#160;&#160;&#160; return repository.Customer.First(c =&gt; c.LastName.StartsWith(lastname));<br>&#125;</span><span><span lang="EN-AU"></span></span><span class="ssw-rteStyle-FigureBad">&#160;Figure&#58; Bad Example - The first comment is only valuable because the method is poorly named, while the second describes *what* is happening, not *why*.</span><span class="ssw-rteStyle-CodeArea">public int GetFirstCustomerWithLastName(string lastname)<br>&#123;<br>&#160;&#160;&#160; <span style="background-color&#58;#ffff00;">// we use StartsWith because the legacy system sometimes padded with spaces</span><br>&#160;&#160;&#160; return repository.Customer.First(c =&gt; c.LastName.StartsWith(lastname));<br>&#125;</span><span class="ssw-rteStyle-FigureGood">Figure&#58; Good Example - The method has been renamed so no comment is required, and the comment explains *why* the code has been written in that way.</span></p>


