---
type: rule
title: Do you know how to upgrade your TFS2010 databases? (the big one)
uri: do-you-know-how-to-upgrade-your-tfs2010-databases-the-big-one
created: 2012-06-02T01:36:36.0000000Z
authors:
- id: 23
  title: Damian Brady

---

 
We recommend doing a [move to a new environment](/TFS/RulesToBetterTFS2012Migration/Pages/MigrationChoices.aspx) because it has a much easier rollback path if something goes wrong.

Note that these steps will also work for upgrading from TFS 2012 RC to RTM, or RTM to Update 1.
 
​These are the steps to migrate and upgrade to a new environment:

1. [Send an email](http&#58;//www.ssw.com.au/SSW/Standards/Rules/RulesToBetterNetworks.aspx#rebootrestart) to let everyone know the TFS server will be offline.
2. Take the TFS 2010 server offline
3. Copy the TFS 2010 database backups to the TFS server or the new SQL Server instance. Make sure the URL is accessible from the TFS server via a network share.
4. Install Team Foundation Server 2012 or TFS 2012 Update 1 ([see Damian Brady's experiences](http&#58;//blog.damianbrady.com.au/2012/11/27/tfs-2012-with-update-1-done/)). Make sure you have access to coffee - it could take a while!
5. After the install has completed, the Team Foundation Server Configuration Center will start
6. Select Upgrade | Start Wizard
![tfs_upgrade_existing.png](/TFS/RulesToBetterTFS2012Migration/PublishingImages/tfs_upgrade_existing.png)
7. Launch the Database Restore tool by clicking on the link
8. If necessary, change the Target SQL Server Instance and click Connect
9. In the Restore Database screen, Browse, then navigate to the folder with your database backups. Make sure all of them are ticked, then click Restore.
![tfs_restore_dbs.png](/TFS/RulesToBetterTFS2012Migration/PublishingImages/tfs_restore_dbs.png)
10. Click Close, then click Next in the Upgrade Wizard
11. Choose the configuration database by specifying the SQL Server Instance and clicking List Available Databases
12. Check "By checking this box, I confirm that I have a current backup.", then click Next
![tfs_config_db.png](/TFS/RulesToBetterTFS2012Migration/PublishingImages/tfs_config_db.png)
13. Leave Network Service as the service account for the Application Tier, then click Next
14. Check the checkbox to confirm we want to configure Reporting Services, then click Next
15. Make sure the Reporting Services instance and URLs are correct, then click Next
![tfs_config_reporting.png](/TFS/RulesToBetterTFS2012Migration/PublishingImages/tfs_config_reporting.png)
16. Update the SQL Server Instance for our Warehouse Database, and click Test to test the connection
17. Click List Available Databases and check the Tfs\_Warehouse database is shown, then click Next
![tfs_warehouse.png](/TFS/RulesToBetterTFS2012Migration/PublishingImages/tfs_warehouse.png)
18. Click Next on the Analysis Services page
19. Provide details of the TFSService account your reports will run as then click Next
![tfs_reports_run_as.png](/TFS/RulesToBetterTFS2012Migration/PublishingImages/tfs_reports_run_as.png)
20. Check the checkbox to say we want to configure SharePoint, then click Next
21. Choose "Use current SharePoint settings", then click Next
![tfs_sharepoint.png](/TFS/RulesToBetterTFS2012Migration/PublishingImages/tfs_sharepoint.png)
22. Confirm the details on the Summary page and click Verify
![tfs_summary.png](/TFS/RulesToBetterTFS2012Migration/PublishingImages/tfs_summary.png)
**Note:** At this point, you may be asked to reboot and start the wizard again.  Don't despair - it's quicker the second time!
23. Once you have all green ticks, click Configure
![tfs_final_configure.png](/TFS/RulesToBetterTFS2012Migration/PublishingImages/tfs_final_configure.png)
24. Have a coffee
![coffee.png](/TFS/RulesToBetterTFS2010Migration/PublishingImages/ssw-coffee.png)
25. Click Next
![tfs_upgrade_complete.png](/TFS/RulesToBetterTFS2012Migration/PublishingImages/tfs_upgrade_complete.png)
26. Click Close, then Close again.
27. Change the DNS entries for your TFS server to point to the new TFS 2012 server
![tfs_dns.png](/TFS/RulesToBetterTFS2012Migration/PublishingImages/tfs_dns.png)
**Note:** It's a good idea to get the SysAdmins involved at this stage


