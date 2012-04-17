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

 We all know it’s important to keep our servers updated. Unfortunately though, by default, Windows will automatically download and install all new Windows Updates on your servers. This will mean the servers will occasionally restart to install updates when you don’t want them too. You will also get annoying popups trying to get you to restart the computer.  ![ Accidently press Restart Now on a Production server and your users won't be happy!](/PublishingImages/updates-restart.jpg) 
Accidently press Restart Now on a Production server and your users won't be happy!
The best ensure you are still downloading updates but not installing them automatically is to use Group Policy. 


1. Create an Organization Unit (OU) in Active Directory, and put all your Production Servers in the OU
![Add all your Production Servers to the Production Server OU](/PublishingImages/updates-adou.jpg)
Add all your Production Servers to the Production Server OU
2. Create a new Group Policy object and link it to the Production Server OU
![Create a new Group Policy for your Production Servers](/PublishingImages/updates-gpo.jpg)
Create a new Group Policy for your Production Servers
3. Edit the new Group Policy object and drill down to **Computer Configuration** | **Policies **| **Windows Components** | **Windows Update**
4. Edit the **Configure Automatic Update Properties** item and **enable **it
5. Set the **Configure Automatic Updating** option to **3 – Auto download and notify for install
![Edit Configure Automatic Updates Properties and enable 'Auto download and notify for install'](/PublishingImages/updates-editgp.jpg)
**Edit Configure Automatic Updates Properties and enable 'Auto download and notify for install

 After the new Group Policy propagates, you will notice the update setting is now locked on the servers in the Production Server OU. 

![The Group Policy locks the Windows Update setting](/PublishingImages/updates-updatesforced.jpg)
The Group Policy locks the Windows Update setting

Now the next time you plan to reboot your server you can install updates quickly and reboot – keeping your servers updated without unplanned reboots.

The following screenshot is the settings applied to the default domain policy for the same group policy settings but this will apply to all machines joined to the SSW domain. ![Default domain policy1.png](/Documents/Default%20domain%20policy1.png)



