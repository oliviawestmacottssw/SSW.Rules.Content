---
type: rule
title: Do you backup your databases?
uri: do-you-backup-your-databases
created: 2009-11-07T23:06:18.0000000Z
authors: []

---



Run your daily backups to provide a saftey net should things go wrong.

1. Confirm that the TFS2008 databases were backed up last night. a. TfsActivityLogging
<br>    b. TfsBuild
<br>    c. TfsIntegration
<br>    d. TfsVersionControl
<br>    e. TfsWarehouse 
<br>    f. TfsWorkItemTracking
<br>    g. TfsWorkItemTrackingAttachmentsFigure: If you can’t see the physical .bak file for all these, chase up your DBA
2. Create a backup of the TFS2008 databases by running your Daily Backup maintenance plan on TFS2008 
![](/TFS/RulesToBetterTFS2010Migration/PublishingImages/RunDailyBackup.png)
Figure 1 - Before starting, kick off the daily backups



