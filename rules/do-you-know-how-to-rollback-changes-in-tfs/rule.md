---
type: rule
title: Do you know how to rollback changes in TFS?
uri: do-you-know-how-to-rollback-changes-in-tfs
created: 2011-11-18T03:52:54.0000000Z
authors:
- id: 22
  title: David Klein
- id: 5
  title: Justin King
- id: 17
  title: Ryan Tee
- id: 6
  title: Tristan Kurniawan

---

 This field should not be null (Remove me when you edit this field). 
There are two ways to do this:1. If you haven’t checked in any files since you started modifying them then the process is simple:
    - Right click your solution and **Undo Pending Changes**![Undo Pending changes](/PublishingImages/rollback1.gif)
2. If you aren’t so lucky and have made some commits along the way then the only option is to use the Rollback command.
    - To use this you will need to install [Team Foundation Server Power Tools v1.2](http&#58;//www.ssw.com.au/ssw/Redirect/TFSPowerToolsDownload.htm) ![](http&#58;//www.ssw.com.au/ssw/images/external.gif "You are now leaving SSW")
    - Find the revision before you started checking code in using the **History command**![Revision List](/PublishingImages/rollback2.gif)Figure: The last revision before Tristan made changes was 5367
    - Open the Command Prompt in your current working directory and type **“c:\Program Files\Microsoft Team Foundation Server Power Tools\tfpt.exe” rollback /changeset:5367**![Rollback Changeset](/PublishingImages/rollback3.gif)
    - Click **Yes** and the rollback will proceed


It would be nice if there was a GUI for this tool so that I can just right click and select rollback. See [Better Software Suggestion – TFS](http&#58;//www.ssw.com.au/ssw/Standards/BetterSoftwareSuggestions/TeamFoundationServer.aspx#RollbackGUI)

