---
type: rule
title: Do you check your Workspaces when defining a new build?
uri: do-you-check-your-workspaces-when-defining-a-new-build
created: 2012-03-28T05:38:50.0000000Z
authors:
- id: 23
  title: Damian Brady
- id: 28
  title: Daragh Bannigan

---

 
​When defining a build, you should always check the Workspace tab. Only the workspace relevant to your build should be included.
   ​ 
If you have a number of Team Projects open from the same TFS Project Collection, all of their workspaces will be included by default.  You should remove those workspaces that aren’t being used otherwise the build server will get the source for every workspace in this list before starting a build.

 ![](/PublishingImages/bad_workspace.png)
   ![](/PublishingImages/bad.gif)**Figure: Bad example – Several workspaces from other team projects are included by default**

 

![](/PublishingImages/good_workspace.png)
**  ![](/PublishingImages/good.gif)Figure: Good example – Only the relevant workspace has been included in this build definition**

