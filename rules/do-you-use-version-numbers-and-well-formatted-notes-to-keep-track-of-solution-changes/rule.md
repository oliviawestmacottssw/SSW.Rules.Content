---
type: rule
archivedreason: 
title: Do you use version numbers and well formatted notes to keep track of solution changes?
guid: 0cbd73ec-a509-4e06-92e6-d683e8d39e2b
uri: do-you-use-version-numbers-and-well-formatted-notes-to-keep-track-of-solution-changes
created: 2020-07-02T23:39:06.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
- title: Mehmet Ozdemir
  url: https://ssw.com.au/people/mehmet-ozdemir
related: []
redirects: []

---


<p class="ssw15-rteElement-P">Dynamics uses a solution as a logical container to hold all customizations for a given function or sub-function. It is very important to have a versioning strategy around changes and when to increment versions.​<br></p>
<br><excerpt class='endintro'></excerpt><br>
<p class="ssw15-rteElement-P">Increment the version *every time* a change is made and add a new line at the top of the description field containing:​​<br></p><ol><li>New version number </li><li>Developer initials </li><li>​Change notes, can changes, removals, additions to the solution </li></ol><p class="ssw15-rteElement-P">This gives you a quick and easy reference for the changes that have happened in the solution. Following this standard means comparing solutions across environments is a painless process.</p><p></p><dl class="badImage"><dt>​<img src="change-log-bad.png" alt="change-log-bad.png" style="width:750px;" /></dt><dd>Bad Example: Version 1.0.0.0, No change​log</dd></dl><dl class="goodImage"><dt><img src="change-log-good.png" alt="change-log-good.png" style="width:750px;" /></dt><dd>Good Example: Solution has up to date versioning with detailed changelog<br></dd></dl>


