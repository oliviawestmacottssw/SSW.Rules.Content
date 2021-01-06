---
type: rule
archivedreason: 
title: Do you use Group Policy to manage your Windows Update Policy?
guid: 19452101-3232-446e-9932-2e8486b410d4
uri: do-you-use-group-policy-to-manage-your-windows-update-policy
created: 2011-03-21T00:27:18.0000000Z
authors:
- title: Matthew Hodgkins
  url: https://ssw.com.au/people/matthew-hodgkins
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
related: []
redirects: []

---

We all know it’s important to keep our servers updated. Unfortunately though, by default, Windows will automatically download and install all new Windows Updates on your servers. This will mean the servers will occasionally restart to install updates when you don’t want them too. You will also get annoying popups trying to get you to restart the computer. 

<!--endintro-->

**Note:** This rule applied to both client PCs and servers.




It is also one more reason developers don’t like to join a company domain on their personal laptops!


<dl class="badImage"><dt> 
      <img alt="Windows-Update-notification.png" src="Windows-Update-notification.png" style="width:750px;"> 
   </dt><dd>Bad Example - Windows 10 shows a ‘Restart now’ – do not accidentally press it! Your production server and your users won't be happy!</dd></dl><dl class="badImage"><dt><img src="updates-restart.jpg" alt="Accidently press Restart Now on a Production server and your users won't be happy!"> </dt><dd>Bad example – Remember this nasty one from Vista days?</dd></dl>
**Note:** Server patching is also achievable via SCCM and you get more control over restarting windows like this. WSUS can also be used in conjunction with group policies to handle restart times better.

The best ensure you are still downloading updates but not installing them automatically is to use Group Policy.

1. Create an Organization Unit (OU) in Active Directory, and put all your Production Servers in the OU
<dl class="image"><dt> 
            <img src="updates-adou.jpg" alt="Add all your Production Servers to the Production Server OU"> 
         </dt><dd>Add all your Production Servers to the Production Server OU</dd></dl>
2. Create a new Group Policy object and link it to the Production Server OU
<dl class="image"><dt> 
            <img src="updates-gpo.jpg" alt="Create a new Group Policy for your Production Servers"> 
         </dt><dd>Create a new Group Policy for your Production Servers</dd></dl>
3. Edit the new Group Policy object and drill down to <br>       **Computer Configuration** | <br>       **Policies** | <br>       **Windows Components** | <br>       **Windows Update**
4. Edit the <br>       **Configure Automatic Update Properties** item and <br>       **enable** it
5. Set the <br>       **Configure Automatic Updating** option to <br>       **3 – Auto download and notify for install
<dl class="image"><dt> 
               <img src="updates-editgp.jpg" alt="Edit Configure Automatic Updates Properties and enable Auto download and notify for install"> 
            </dt><dd>Edit Configure Automatic Updates Properties and enable 'Auto download and notify for install</dd></dl>**


After the new Group Policy propagates, you will notice the update setting is now locked on the servers in the Production Server OU.
<dl class="goodImage"><dt> 
      <img src="updates-updatesforced.jpg" alt="The Group Policy locks the Windows Update setting"> 
   </dt><dd>The Group Policy locks the Windows Update setting</dd></dl>


From now on your servers will be updated without unplanned reboots!
<dl class="image"><dt> 
      <img src="Default domain policy1.png" alt="Default domain policy1.png">
   </dt><br><br>::: good<br>     Figure: Good example - AD shows the Group Policy setting “3 – Auto download and notify for install”. This policy is applied to the specified OU eg. Production Servers joined to this domain 
      <br><br>:::<br><br></dl>


###  Related Rules


* [Do you enable automatic Windows Update Installations?](/disable-automatic-Windows-Update-Installations) [for PCs]
* [Do you turn off auto-update on your servers?](/Do-you-turn-off-auto-update-on-your-servers) [for Servers]
