---
type: rule
archivedreason: 
title: Do you know how to upgrade CRM 2015 to 2016
guid: 8623800a-0a9a-49a3-9edc-2d01c78c4dfe
uri: do-you-know-how-to-upgrade-crm-2015-to-2016
created: 2016-01-22T04:02:32.0000000Z
authors: []
related: []
redirects: []

---

CRM 2016 has many improvements over it's predecessors, including Power BI integration, improved navigation, and the new Outlook extension.



The procedure for upgrading CRM 2015 to 2016 is: 
<!--endintro-->



1. Apply Windows Update on CRM and Database servers

2. Go to CRM server | Deployment Manager | Disable CRM organization
<dl class="ssw15-rteElement-ImageArea"><img src="disable_org.png" alt="disable_org.png" style="margin:5px;width:562px;">   <strong>Figure: Disable organization</strong> <strong><dl class="ssw15-rteElement-ImageArea"> <strong><br></strong> </dl></strong> </dl>
3. Back up CRM organization database and configuration database

4. Go to CRM server | Control Panel | Uninstall "Microsoft Dynamics CRM Reporting Extensions"
<dl class="ssw15-rteElement-ImageArea"><img src="uninstall_reportingextensions.png" alt="uninstall_reportingextensions.png" style="margin:5px;width:447px;height:313px;">  <strong>Figure: Uninstall CRM Reporting Extensions</strong> <br><br></dl>
5. Download [CRM 2016 Server installation file](https://www.microsoft.com/en-us/download/details.aspx?id=50372) and start the upgrade
<dl class="ssw15-rteElement-ImageArea"><img src="upgrade_demoorg.png" alt="upgrade_demoorg.png" style="margin:5px;width:473px;height:410px;">  <strong>Figure: Select the demo organization to be upgraded</strong> <p class="ssw15-rteElement-InfoBox">Note: It's better to have an empty demo organization to be upgraded first, so that you can test if the server upgrade has no issues.<br></p></dl><dl class="ssw15-rteElement-ImageArea"><img src="upgrade_successfully.png" alt="upgrade_successfully.png" style="margin:5px;width:401px;height:401px;">  <strong>Figure: Successfully upgraded CRM server</strong> <dl class="ssw15-rteElement-ImageArea"><img src="test_demo_org.png" alt="test_demo_org.png" style="margin:5px;width:568px;height:253px;"> <strong>Figure: Quick test on the demo organization</strong> <strong><dl class="ssw15-rteElement-ImageArea"> <strong><img src="upgrade_businessOrg.png" alt="upgrade_businessOrg.png" style="margin:5px;width:683px;height:169px;">Figure: Upgrade business organization</strong> <strong><dl class="ssw15-rteElement-ImageArea"> <strong><img src="upgrade_org_successfully.png" alt="upgrade_org_successfully.png" style="margin:5px;width:496px;height:363px;">Figure: Successfully upgrade organization</strong> <strong><dl class="ssw15-rteElement-ImageArea"> <strong><br></strong> </dl></strong> </dl></strong> </dl></strong> </dl></dl>
6. Go to CRM setup directory | SrsDataConnector | Install 'Microsoft Dynamics CRM Reporting Extensions"
<dl class="ssw15-rteElement-ImageArea"><img src="install_reporting_extensions.png" alt="install_reporting_extensions.png" style="margin:5px;width:492px;height:305px;">  <strong>Figure: Install CRM Reporting Extensions</strong> <dl><dl class="ssw15-rteElement-ImageArea"><img src="upgrade_to_crm2016.png" alt="upgrade_to_crm2016.png" style="margin:5px;width:698px;height:354px;"> <strong>Figure: Successfully upgraded to CRM2016</strong> <br><br><p class="ssw15-rteElement-InfoBox">If using Email Router, do the following 2 steps to upgrade Email Router to 2016<br></p></dl></dl></dl>
7. Go to CRM server | Uninstall "Microsoft Dynamics CRM 2015 Email Router"
<dl class="ssw15-rteElement-ImageArea"><img src="uninstall_emailRouter.png" alt="uninstall_emailRouter.png" style="margin:5px;width:537px;height:208px;">  <strong>Figure: Uninstall Email Router 2015</strong> <strong><dl class="ssw15-rteElement-ImageArea"> <strong><br></strong> </dl></strong> </dl>
8. Download [CRM 2016 Email Router](https://www.microsoft.com/en-us/download/details.aspx?id=50373) and install
<dl class="ssw15-rteElement-ImageArea"><img src="install_emailRouter.png" alt="install_emailRouter.png" style="margin:5px;line-height:33.6px;width:477px;height:338px;"> <strong>Figure: Install required components for Email Router 2016</strong> </dl><dl class="ssw15-rteElement-ImageArea"><img src="emailRouter_installtionFinish.png" alt="emailRouter_installtionFinish.png" style="margin:5px;width:392px;height:353px;"> <strong>Figure: Successfully installed Email Router 2016</strong> <strong><dl class="ssw15-rteElement-ImageArea"> <strong><img src="configurate_emailrouter_2.png" alt="configurate_emailrouter_2.png" style="margin:5px;width:381px;height:525px;"> Figure: Configure Email Router</strong> </dl></strong> </dl>
You're now ready to roll with Microsoft Dynamics CRM 2016. If you had any trouble with this guide, please let us know with a rating of this rule.
