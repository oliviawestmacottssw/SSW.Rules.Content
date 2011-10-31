---
type: rule
title: Do you use Group Policy to manage your Windows Update Policy?
uri: do-you-use-group-policy-to-manage-your-windows-update-policy
created: 2011-03-21T00:27:18.0000000Z
authors:
- id: 21
  title: Matthew Hodgkins
- id: 1
  title: Adam Cogan

---

 We all know it’s important to keep our servers updated. Unfortunately though, by default, Windows will automatically download and install all new Windows Updates on your servers. This will mean the servers will occasionally restart to install updates when you don’t want them too. You will also get annoying popups trying to get you to restart the computer.  ![ Accidently press Restart Now on a Production server and your users won't be happy!](/ITAndNetworking/RulesToBetterWindowsServers/PublishingImages/updates-restart.jpg) 
Figure 1 - Accidently press Restart Now on a Production server and your users won't be happy!
The best ensure you are still downloading updates but not installing them automatically is to use Group Policy. 


1. Create an Organization Unit (OU) in Active Directory, and put all your Production Servers in the OU
![Add all your Production Servers to the Production Server OU](/ITAndNetworking/RulesToBetterWindowsServers/PublishingImages/updates-adou.jpg)
Figure 2 - Add all your Production Servers to the Production Server OU
2. Create a new Group Policy object and link it to the Production Server OU
![Create a new Group Policy for your Production Servers](/ITAndNetworking/RulesToBetterWindowsServers/PublishingImages/updates-gpo.jpg)
Figure 3 - Create a new Group Policy for your Production Servers
3. Edit the new Group Policy object and drill down to **Computer Configuration** | **Policies **| **Windows Components** | **Windows Update**
4. Edit the **Configure Automatic Update Properties** item and **enable **it
5. Set the **Configure Automatic Updating** option to **3 – Auto download and notify for install
![Edit Configure Automatic Updates Properties and enable 'Auto download and notify for install'](/ITAndNetworking/RulesToBetterWindowsServers/PublishingImages/updates-editgp.jpg)
**Figure 4 - Edit Configure Automatic Updates Properties and enable 'Auto download and notify for install

 After the new Group Policy propagates, you will notice the update setting is now locked on the servers in the Production Server OU. 

![The Group Policy locks the Windows Update setting](/ITAndNetworking/RulesToBetterWindowsServers/PublishingImages/updates-updatesforced.jpg)
Figure 5 - The Group Policy locks the Windows Update setting

Now the next time you plan to reboot your server you can install updates quickly and reboot – keeping your servers updated without unplanned reboots.

![Default domain policy.png](/ITAndNetworking/RulesToBetterWindowsServers/Documents/Default%20domain%20policy.png)
Figure 5 - The Group Policy locks the Windows Update setting

