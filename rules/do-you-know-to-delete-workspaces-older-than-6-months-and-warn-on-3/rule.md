---
type: rule
archivedreason: 
title: Do you know to delete workspaces older than 6 months and warn on 3?
guid: d202fa40-dbec-4392-9eac-7fc878d8e81c
uri: do-you-know-to-delete-workspaces-older-than-6-months-and-warn-on-3
created: 2011-11-18T03:52:39.0000000Z
authors:
- title: David Klein
  url: https://ssw.com.au/people/david-klein
- title: Justin King
  url: https://ssw.com.au/people/justin-king
- title: Ryan Tee
  url: https://ssw.com.au/people/ryan-tee
- title: Tristan Kurniawan
  url: https://ssw.com.au/people/tristan-kurniawan
related: []
redirects: []

---


<p>The more workspaces you have the more load the TFS server is under when users check in and out. TFS has to check all of the workspaces for other checkouts of the same files which can be intensive if you have a lot of workspaces.</p>
<br><excerpt class='endintro'></excerpt><br>
<p>If a developer had code checked out to a workspace that they have not even looked at in months, what is the likelihood that they even remember what changes they were making?</p>
<ul>Why do workspaces build up? <li>Developers use multiple computers </li>
<li>Developers use volatile virtual computers </li>
<li>Developers reinstall their workstation </li>
<li>Developers get new workstations </li>
<li>Developers leave </li></ul>
<ul>Developer checklist: <li>Check workspaces often to see what you don't need </li>
<li>Delete any workspaces you no longer need </li></ul>
<ul>TFS Master Checklist: <li>Delete all workspaces that have not been edited in 6 months </li>
<li>Warn developers for workspaces that have not been accessed in 3 months </li></ul>
<dl><dt><img alt="Longtime Workspaces" src="LongtimeWorkspaces.jpg" /></dt>
<dd>Figure: Bad example - Rebecca has a workspace that has not been accessed in a while </dd></dl>
<dl><dt><img alt="Current Workspaces" src="CurrentWorkspaces.jpg" /></dt>
<dd>Figure: Good example - All of Julian's workspaces are current </dd></dl>
<ol><li>Open VS 2010, File | Source Control | WorkSpaces, click the "Show remote workspaces": <dl><dt><img alt="Manage Workspaces " src="ManageWorkspaces.jpg" /></dt>
<dd>Figure: Manage Workspaces </dd></dl></li>
<li>Keep press "Ctrl", select the workspaces which haven't been used for a long time. </li>
<li>Click "Remove" button.</li></ol>


