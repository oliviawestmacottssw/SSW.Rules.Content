---
type: rule
title: Do you use shared check-outs?
uri: do-you-use-shared-check-outs
created: 2011-11-18T03:52:56.0000000Z
authors:
- id: 22
  title: David Klein
- id: 8
  title: John Liu
- id: 17
  title: Ryan Tee
- id: 6
  title: Tristan Kurniawan

---

 
In conjunction with [regular check-ins](/Pages/CheckinRegularly.aspx), files in source control should never be locked unless absolutely necessary. Use either 'Unchanged - Keep any existing lock' - or 'None - Allow shared checkout'.
 
Only use 'Check Out - Prevent other users from checking out and checking in' when checking out binary files e.g. Word documents or third party compiled dll’s. (This will be the default this will be the selected option due to the inability for binary files to be merged on check in.)
![Check-out settings for files](/PublishingImages/Check-outSettingsForFiles.jpg)Figure: Correct checkout settings at the file level - don't lock files 
Do not enforce single check-out at the project level - make sure the 'Enable multiple check-out' option is ticked under Team Project Settings, Source Control.
![check-out settings for team project](/PublishingImages/Check-outSettingsForTeamProjects.jpg)Figure: Correct check-out settings at the team project level - enable multiple check-out's.
