---
type: rule
title: Do you backup your databases?
uri: do-you-backup-your-databases
created: 2015-08-12T16:20:53.0000000Z
authors: []

---

 
Before starting your upgrade, you should back up all your TFS databases.

​It's important that you backup TFS by using one of the supported methods, to ensure that you can reliably restore your data if needed.
 
**​Tip: **The Team Foundation Server Team Foundation Server 2012 Update 2 and above has a built in Scheduled Backup tool which helps you to easily backup all TFS Databases. For versions prior to TFS 2012 Update 2 you have to use Backups tool from the [TFS Power Tools](http&#58;//visualstudiogallery.msdn.microsoft.com/b1ef7eb2-e084-4cb8-9bc7-06c3bad9148f)   package.

**![tfs scheduled.jpg](/PublishingImages/tfs%20scheduled.jpg)
**

**Figure: TFS Scheduled Backups Tool**

In some cases you won't be able to use this tool e.g. with TFS 2012 Power Tools RTM. This version has a bug which causes a failure of Tfs\_Configuration DB when you try to restore it.

![tfs backup.jpg](/PublishingImages/tfs%20backup.jpg)

**Figure: TFS Backup tool failed to restore the Tfs\_Configuration DB – known bug in TFS 2012 Power Tools RTM**

In such case you will have to manually backup databases. Make sure all relevant databases have been backed up. This includes all those starting with "Tfs\_"

**
**

**![backup all.jpg](/PublishingImages/backup%20all.jpg)**

**Figure: Backup all relevant databases**

IMPORTANT

Manual backup requires additional user steps which involve creation of additional tables and stored procedures. These tables has to be created to keep TFS databases in sync.
 Follow this instructions to properly backup your databases:[Manually back up Team Foundation Server](http&#58;//msdn.microsoft.com/en-us/library/ms253070.aspx)  .

**
**

**![add tbl.jpg](/PublishingImages/add%20tbl.jpg)**

**Figure: Add tbl\_TfsTransactionLogMark table to every Tfs\_\* Database**

**![add spset.jpg](/PublishingImages/add%20spset.jpg)
**

**Figure: Add sp\_SetTransactionLogMark stored procedure to every Tfs\_\* Database**

If you manually backup the TFS Databases make sure you add additional jobs that execute 1 minute before the backup kick off.

![add additional.jpg](/PublishingImages/add%20additional.jpg)

**Figure: Add additional jobs to SQL Server Agent**

Make sure you back up the Reporting Services database if you'd like your reports to come across as well.

For Reporting Services make sure you have backed up the encryption key.

![backup reporting.jpg](/PublishingImages/backup%20reporting.jpg)

**Figure: Backup Reporting Services encryption keys**

