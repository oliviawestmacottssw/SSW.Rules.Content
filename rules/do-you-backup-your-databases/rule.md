---
type: rule
title: Do you backup your databases?
uri: do-you-backup-your-databases
created: 2009-11-07T23:06:18.0000000Z
authors: []

---

 

Run your daily backups to provide a safety net should things go wrong.

1. Confirm that the TFS2008 databases were backed up last night. 
a. TfsActivityLogging
b. TfsBuild
c. TfsIntegration
d. TfsVersionControl
e. TfsWarehouse 
f. TfsWorkItemTracking
g. TfsWorkItemTrackingAttachments
Figure: If you can’t see the physical .bak file for all these, chase up your DBA
2. Create a backup of the TFS2008 databases by running your Daily Backup maintenance plan on TFS2008 
![](RunDailyBackup.png)
Figure: Before starting, kick off the daily backups


 
