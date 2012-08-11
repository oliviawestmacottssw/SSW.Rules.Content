---
type: rule
title: Do you know how to upgrade your TFS2008 databases?
uri: do-you-know-how-to-upgrade-your-tfs2008-databases
created: 2009-11-08T00:23:52.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 3
  title: Eric Phan

---

 
Since [we recommend doing a "move based upgrade"](/Pages/MigrationChoices.aspx), we don’t like the "in place upgrade" option, these are the steps:

1. Copy the TFS2008 backups to TFS2010 server (e.g. C:\TfsBackups)
2. Restore all the databases to TFS2010’s instance of SQL 2008
3. Install Team Foundation Server 2010
4. After the install has completed the Team Foundation Server Configuration Wizard will open
5. Select Upgrade | Start Wizard
![TFS Config - Upgrade](/PublishingImages/01-TFS%20Config%20-%20Upgrade.png)
6. Click "Next"
![](/PublishingImages/02-TFS%20Upgrade%20Wizard%20-%20Upgrade.png)
7. Click "List Available Databases"
8. Select the TfsIntegration database
9. Check "By checking this box, I confirm that I have a current backup"
10. Click "Next"
![](/PublishingImages/03-TFS%20Upgrade%20Wizard%20-%20Databases.png)
11. Select "NT AUTHORITY\NETWORK SERVICE" for the System account
12. Click "Next" 
![TFS Upgrade Wizard - Account](/PublishingImages/04-TFS%20Upgrade%20Wizard%20-%20Account.png)
13. Click "Next"
![TFS Upgrade Wizard - Application Tier](/PublishingImages/05-TFS%20Upgrade%20Wizard%20-%20Application%20Tier.png)
14. Click "Next"
![TFS Upgrade Wizard - Reporting](/PublishingImages/06-TFS%20Upgrade%20Wizard%20-%20Reporting.png)
15. Click "Next"
![TFS Upgrade Wizard - Reporting - Reporting Services](/PublishingImages/07-TFS%20Upgrade%20Wizard%20-%20Reporting%20-%20Reporting%20Services.png)
16. Click "Next"
![TFS Upgrade Wizard - Reporting - Analysis Services](/PublishingImages/08-TFS%20Upgrade%20Wizard%20-%20Reporting%20-%20Analysis%20Services.png)
17. Specify the TFSService account
18. Click "Next"
![TFS Upgrade Wizard - Reporting - Report Reader Account](/PublishingImages/09-TFS%20Upgrade%20Wizard%20-%20Reporting%20-%20Report%20Reader%20Account.png)
19. Click "Next"
![TFS Upgrade Wizard - Sharepoint](/PublishingImages/10-TFS%20Upgrade%20Wizard%20-%20Sharepoint.png)
20. Click "Next"
![TFS Upgrade Wizard - Sharepoint - Settings](/PublishingImages/11-TFS%20Upgrade%20Wizard%20-%20Sharepoint%20-%20Settings.png)
21. Click "Next"
![TFS Upgrade Wizard - Project Collection](/PublishingImages/12-TFS%20Upgrade%20Wizard%20-%20Project%20Collection.png)
22. Click "Next"
![TFS Upgrade Wizard - Review](/PublishingImages/13-TFS%20Upgrade%20Wizard%20-%20Review.png)
23. Click "Configure"
![TFS Upgrade Wizard - Readiness Checks](/PublishingImages/14-TFS%20Upgrade%20Wizard%20-%20Readiness%20Checks.png)
24. Have coffee (2 hours)
![Coffee](/PublishingImages/ssw-coffee.png)
BTW: A good user interface should have a coffee image 
[TODO: Martin to create new rule in "Rules to better UI"]
[TODO: Martin to add suggestion to TFS]
![TFS Upgrade Wizard - Configure - Upgrade Process](/PublishingImages/15-TFS%20Upgrade%20Wizard%20-%20Configure%20-%20Upgrade%20Process.png)
25. Click "Next"
![TFS Upgrade Wizard - Configure - Upgrade Process Success](/PublishingImages/16-TFS%20Upgrade%20Wizard%20-%20Configure%20-%20Upgrade%20Process%20Success.png)
26. Click "Close"
![TFS Upgrade Wizard - Complete](/PublishingImages/17-TFS%20Upgrade%20Wizard%20-%20Complete.png)
27. Click "Close"
![TFS Config - Application Server Complete](/PublishingImages/18-TFS%20Config%20-%20Application%20Server%20Complete.png)
28. Change the DNS entry for tfs.northwind.com to point to TFS2010 on
    1. Internal DNS
    2. External DNS



| ![Red Bull Can](/PublishingImages/redbull.jpg) | Since you have to deal with your system admins, this job will take the longest. Speed it up by buying a Red Bull for your system admin |
| --- | --- |


