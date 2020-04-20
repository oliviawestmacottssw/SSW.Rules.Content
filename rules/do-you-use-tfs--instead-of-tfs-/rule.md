

---
authors:
  - id: 10
    title: Lei Xu
---




<span class='intro'> <p>With the release of TFS 2012, you should always use TFS 2012 instead of TFS 2010. </p><p>These are the top 3 features&#58;</p> </span>

<p>​<strong>Local workspaces </strong><br>Local workspaces allow many operations to be done offline (add, edit, rename, delete, undo, diff) and are recommended only for workspaces with fewer 50,000 files.&#160; Local workspaces are now the default with TFS 2012, but you can control that if you want server workspaces to be the default.</p><p><strong>Async checkout for Server Workspaces<br></strong>There is a new TFS 2012 feature so that VS 2012 will do checkouts in the background for server workspaces.&#160; That eliminates the pause when you start typing and VS checks out the file.&#160; Turning it on turns off checkout locks, but you can still use checkin locks.&#160; </p><p><strong>Merge on Unshelve</strong> <br>Shelvesets can now be unshelved into a workspace even if there are local changes on files in the shelveset.&#160; Conflicts will be created for any items modified both locally and in the shelveset, and you will resolve them as you would any other conflict. </p>

