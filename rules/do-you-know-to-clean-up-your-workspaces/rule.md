---
type: rule
title: Do you know to clean up your workspaces?
uri: do-you-know-to-clean-up-your-workspaces
created: 2011-11-18T03:52:31.0000000Z
authors:
- id: 22
  title: David Klein
- id: 5
  title: Justin King
- id: 17
  title: Ryan Tee
- id: 6
  title: Tristan Kurniawan
- id: 23
  title: Damian Brady

---

 This field should not be null (Remove me when you edit this field). 
Every Workspace that exists on the server is another set of code that TFS has to check for checkouts. Worse you may have files checked out in that workspace that you will never see.
![The current workspace status ](/TFS/RulesToBetterVersionControlwithTFS(AKASourceControl)/PublishingImages/WorkspaceStatus.jpg)Figure: John has not accessed many of these workspaces in years! Are they still current? 
Use the Workspace Sidekick in [Team Foundation Sidekicks](http&#58;//www.attrice.info/cm/tfs/index.htm) ![](http&#58;//www.ssw.com.au/ssw/images/external.gif "You are now leaving SSW") at the end of every month to make sure you have not forgotten anything.

