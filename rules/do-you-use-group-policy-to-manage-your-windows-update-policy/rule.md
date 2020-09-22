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

 We all know it’s important to keep our servers updated. Unfortunately though, by default, Windows will automatically download and install all new Windows Updates on your servers. This will mean the servers will occasionally restart to install updates when you don’t want them too. You will also get annoying popups trying to get you to restart the computer. 
 
**Note:** This rule applied to both client PCs and servers.




It is also one more reason developers don’t like to join a company domain on their personal laptops!


![Windows-Update-notification.png](Windows-Update-notification.png)Bad Example - Windows 10 shows a ‘Restart now’ – do not accidentally press it! Your production server and your users won't be happy!​![Accidently press Restart Now on a Production server and your users won't be happy!](updates-restart.jpg) Bad example – Remember this nasty one from Vista days?
**Note: **Server patching is also achievable via SCCM and you get more control over restarting windows like this. WSUS can also be used in conjunction with group policies to handle restart times better.

The best ensure you are still downloading updates but not installing them automatically is to use Group Policy.

1. Create an Organization Unit (OU) in Active Directory, and put all your Production Servers in the OU
![Add all your Production Servers to the Production Server OU](updates-adou.jpg)Add all your Production Servers to the Production Server OU
2. Create a new Group Policy object and link it to the Production Server OU
![Create a new Group Policy for your Production Servers](updates-gpo.jpg)Create a new Group Policy for your Production Servers
3. Edit the new Group Policy object and drill down to <br>      **Computer Configuration** | <br>      **Policies **| <br>      **Windows Components** | <br>      **Windows Update**
4. Edit the <br>      **Configure Automatic Update Properties** item and <br>      **enable **it
5. Set the <br>      **Configure Automatic Updating** option to <br>      **3 – Auto download and notify for install
![Edit Configure Automatic Updates Properties and enable Auto download and notify for install](updates-editgp.jpg)Edit Configure Automatic Updates Properties and enable 'Auto download and notify for install **


After the new Group Policy propagates, you will notice the update setting is now locked on the servers in the Production Server OU.
![The Group Policy locks the Windows Update setting](updates-updatesforced.jpg)The Group Policy locks the Windows Update setting


From now on your servers will be updated without unplanned reboots!
![Default domain policy1.png](Default domain policy1.png)     Figure: Good example - AD shows the Group Policy setting “3 – Auto download and notify for install”. This policy is applied to the specified OU eg. Production Servers joined to this domain <br>      



###  ​​Related Rules


- [​Do you enable automatic Windows Update Installations?​](/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&TermId=f5432cb4-40af-491b-8da5-33b8a80dcb0a) [for PCs]
- [Do you turn off auto-update on your servers?](/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&TermId=3b0722be-c3e3-4369-a590-258c7501a67a) [for Servers]​


