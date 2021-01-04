---
type: rule
archivedreason: 
title: Do you use shared check-outs?
guid: 478af762-d746-48c0-a56b-967d52086e90
uri: do-you-use-shared-check-outs
created: 2011-11-18T03:52:56.0000000Z
authors:
- title: David Klein
  url: https://ssw.com.au/people/david-klein
- title: John Liu
  url: https://ssw.com.au/people/john-liu
- title: Ryan Tee
  url: https://ssw.com.au/people/ryan-tee
- title: Tristan Kurniawan
  url: https://ssw.com.au/people/tristan-kurniawan
related: []
redirects: []

---


<p>In conjunction with <a href="/Pages/CheckinRegularly.aspx">regular check-ins</a>, files in source control should never be locked unless absolutely necessary. Use either 'Unchanged - Keep any existing lock' - or 'None - Allow shared checkout'.</p>
<br><excerpt class='endintro'></excerpt><br>
<p>Only use 'Check Out - Prevent other users from checking out and checking in' when checking out binary files e.g. Word documents or third party compiled dll’s. (This will be the default this will be the selected option due to the inability for binary files to be merged on check in.)</p>
<dl><dt><img alt="Check-out settings for files" src="Check-outSettingsForFiles.jpg" width="607" height="386" /></dt>
<dd>Figure: Correct checkout settings at the file level - don't lock files </dd></dl>
<p>Do not enforce single check-out at the project level - make sure the 'Enable multiple check-out' option is ticked under Team Project Settings, Source Control. </p>
<dl><dt><img alt="check-out settings for team project" src="Check-outSettingsForTeamProjects.jpg" width="666" height="170" /></dt>
<dd>Figure: Correct check-out settings at the team project level - enable multiple check-out's.</dd></dl>


