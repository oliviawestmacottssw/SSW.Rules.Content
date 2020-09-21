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



<span class='intro'> <div>Since <a href="/Pages/MigrationChoices.aspx" shape="rect">we recommend doing a &quot;move based upgrade&quot;</a>, we don’t like the &quot;in place upgrade&quot; option, these are the steps&#58;</div>
<div><ol><li>Copy the TFS2008 backups to TFS2010 server (e.g. C&#58;\TfsBackups) </li>
<li>Restore all the databases to TFS2010’s instance of SQL 2008 </li>
<li>Install Team Foundation Server 2010 </li>
<li>After the install has completed the Team Foundation Server Configuration Wizard will open </li>
<li>Select Upgrade | Start Wizard<br><span><img alt="TFS Config - Upgrade" src="01-TFS Config - Upgrade.png" style="width&#58;500px;height&#58;375px;" /></span> </li>
<li><span>Click &quot;Next&quot;<br><span><img src="02-TFS Upgrade Wizard - Upgrade.png" alt="" style="width&#58;500px;height&#58;375px;" /></span></span> </li>
<li><span><span>Click &quot;List Available Databases&quot;</span></span> </li>
<li><span><span>Select the TfsIntegration database</span></span> </li>
<li><span><span>Check &quot;By checking this box, I confirm that I have a current backup&quot;</span></span> </li>
<li><span><span>Click &quot;Next&quot;<br><span><img src="03-TFS Upgrade Wizard - Databases.png" alt="" style="width&#58;500px;height&#58;375px;" /></span></span></span> </li>
<li><span><span><span>Select &quot;NT AUTHORITY\NETWORK SERVICE&quot; for the System account</span></span></span> </li>
<li><span><span><span>Click &quot;Next&quot;&#160;<br><span><img alt="TFS Upgrade Wizard - Account" src="04-TFS Upgrade Wizard - Account.png" style="width&#58;500px;height&#58;375px;" /></span></span></span></span> </li>
<li><span><a shape="rect" name="StartMigration"></a>Click &quot;Next&quot;<br><img alt="TFS Upgrade Wizard - Application Tier" src="05-TFS Upgrade Wizard - Application Tier.png" style="width&#58;500px;height&#58;375px;" /></span> </li>
<li><span><span><span><span><span>Click &quot;Next&quot;<br><span><img alt="TFS Upgrade Wizard - Reporting" src="06-TFS Upgrade Wizard - Reporting.png" style="width&#58;500px;height&#58;375px;" /></span></span></span></span></span></span> </li>
<li><span><span><span><span><span><span>Click &quot;Next&quot;<br><span><img alt="TFS Upgrade Wizard - Reporting - Reporting Services" src="07-TFS Upgrade Wizard - Reporting - Reporting Services.png" style="width&#58;500px;height&#58;375px;" /></span></span></span></span></span></span></span> </li>
<li><span><span><span><span><span><span><span>Click &quot;Next&quot;<br><span><img alt="TFS Upgrade Wizard - Reporting - Analysis Services" src="08-TFS Upgrade Wizard - Reporting - Analysis Services.png" style="width&#58;500px;height&#58;375px;" /></span></span></span></span></span></span></span></span> </li>
<li><span><span><span><span><span><span><span><span>Specify the TFSService account</span></span></span></span></span></span></span></span> </li>
<li><span><span><span><span><span><span><span><span>Click &quot;Next&quot;<br><span><img alt="TFS Upgrade Wizard - Reporting - Report Reader Account" src="09-TFS Upgrade Wizard - Reporting - Report Reader Account.png" style="width&#58;500px;height&#58;375px;" /></span></span></span></span></span></span></span></span></span> </li>
<li><span><span><span><span><span><span><span><span><span>Click &quot;Next&quot;<br><span><img alt="TFS Upgrade Wizard - Sharepoint" src="10-TFS Upgrade Wizard - Sharepoint.png" style="width&#58;500px;height&#58;375px;" /></span></span></span></span></span></span></span></span></span></span> </li>
<li><span><span><span><span><span><span><span><span><span><span>Click &quot;Next&quot;<br><span><img alt="TFS Upgrade Wizard - Sharepoint - Settings" src="11-TFS Upgrade Wizard - Sharepoint - Settings.png" style="width&#58;500px;height&#58;375px;" /></span></span></span></span></span></span></span></span></span></span></span> </li>
<li><span><span><span><span><span><span><span><span><span><span><span>Click &quot;Next&quot;<br><span><img alt="TFS Upgrade Wizard - Project Collection" src="12-TFS Upgrade Wizard - Project Collection.png" style="width&#58;500px;height&#58;375px;" /></span></span></span></span></span></span></span></span></span></span></span></span> </li>
<li><span><span><span><span><span><span><span><span><span><span><span><span>Click &quot;Next&quot;<br><span><img alt="TFS Upgrade Wizard - Review" src="13-TFS Upgrade Wizard - Review.png" style="width&#58;500px;height&#58;375px;" /></span></span></span></span></span></span></span></span></span></span></span></span></span> </li>
<li><span><span><span><span><span><span><span><span><span><span><span><span><span>Click &quot;Configure&quot;<br><span><img alt="TFS Upgrade Wizard - Readiness Checks" src="14-TFS Upgrade Wizard - Readiness Checks.png" style="width&#58;500px;height&#58;375px;" /></span></span></span></span></span></span></span></span></span></span></span></span></span></span> </li>
<li><span><span><span><span><span><span><span><span><span><span><span><span><span><span>Have coffee (2 hours)<br><span><img alt="Coffee" src="ssw-coffee.png" style="width&#58;200px;" /></span><br>BTW&#58; A good user interface should have a coffee image <br>[TODO&#58; Martin to create new rule in &quot;Rules to better UI&quot;]<br>[TODO&#58; Martin to add suggestion to TFS]<br><img alt="TFS Upgrade Wizard - Configure - Upgrade Process" src="15-TFS Upgrade Wizard - Configure - Upgrade Process.png" style="width&#58;500px;height&#58;376px;" /></span></span></span></span></span></span></span></span></span></span></span></span></span></span> </li>
<li><span><span><span><span><span><span><span><span><span><span><span><span><span><span>Click &quot;Next&quot;<br><span><img alt="TFS Upgrade Wizard - Configure - Upgrade Process Success" src="16-TFS Upgrade Wizard - Configure - Upgrade Process Success.png" style="width&#58;500px;height&#58;374px;" /></span><br></span></span></span></span></span></span></span></span></span></span></span></span></span></span></li>
<li><span><span><span><span><span><span><span><span><span><span><span><span><span><span><span>Click &quot;Close&quot;<br><span><img alt="TFS Upgrade Wizard - Complete" src="17-TFS Upgrade Wizard - Complete.png" style="width&#58;500px;height&#58;375px;" /></span></span></span></span></span></span></span></span></span></span></span></span></span></span></span></span> </li>
<li><span><span><span><span><span><span><span><span><span><span><span><span><span><span><span><span>Click &quot;Close&quot;<br><span><img alt="TFS Config - Application Server Complete" src="18-TFS Config - Application Server Complete.png" style="width&#58;500px;height&#58;375px;" /></span></span></span></span></span></span></span></span></span></span></span></span></span></span></span></span></span> </li>
<li><span><span><span><span><span><span><span><span><span><span><span><span><span><span><span><span><span>Change the DNS entry for tfs.northwind.com to point to TFS2010 on</span></span></span></span></span></span></span></span></span></span></span></span></span></span></span></span></span> <ol><li><span><span><span><span><span><span><span><span><span><span><span><span><span><span><span><span><span>Internal DNS</span></span></span></span></span></span></span></span></span></span></span></span></span></span></span></span></span> </li>
<li><span><span><span><span><span><span><span><span><span><span><span><span><span><span><span><span><span>External DNS</span></span></span></span></span></span></span></span></span></span></span></span></span></span></span></span></span> </li></ol>
<div><table><tbody><tr><td style="width&#58;32px;height&#58;32px;"><img alt="Red Bull Can" src="redbull.jpg" style="width&#58;32px;height&#58;32px;" /></td>
<td>Since you have to deal with your system admins, this job will take the longest. Speed it up by buying a Red Bull for your system admin</td></tr></tbody></table></div></li></ol></div>
 </span>




