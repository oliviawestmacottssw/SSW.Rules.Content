---
type: rule
title: Do you use TFS 2012 instead of TFS 2010?
uri: do-you-use-tfs-2012-instead-of-tfs-2010
created: 2009-11-05T06:35:33.0000000Z
authors:
- id: 10
  title: Lei Xu

---

 
With the release of TFS 2012, you should always use TFS 2012 instead of TFS 2010. 

**Async checkout**
There is a new TFS 2012 feature so that VS 2012 will do checkouts in the background for server workspaces.  That eliminates the pause when you start typing and VS checks out the file.  Turning it on turns off checkout locks, but you can still use checkin locks.

**Merge on Unshelve** 
Shelvesets can now be unshelved into a workspace even if there are local changes on files in the shelveset.  Conflicts will be created for any items modified both locally and in the shelveset, and you will resolve them as you would any other conflict.

**Local workspaces **
Local workspaces allow many operations to be done offline (add, edit, rename, delete, undo, diff) and are recommended only for workspaces with fewer 50,000 files.  Local workspaces are now the default with TFS 2012, but you can control that if you want server workspaces to be the default.
 
