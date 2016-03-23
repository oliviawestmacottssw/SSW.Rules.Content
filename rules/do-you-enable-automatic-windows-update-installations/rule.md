---
type: rule
title: Do you enable automatic Windows Update Installations?
uri: do-you-enable-automatic-windows-update-installations
created: 2014-08-29T20:08:15.0000000Z
authors:
- id: 40
  title: Igor Goldobin
- id: 47
  title: Stanley Sidik

---

 
​​Microsoft automatic updates can be dangerous.

Microsoft Update is a service that allows for the periodic patching of system files to address known issues with Microsoft products. Originally called Windows Update, it was specifically focused on Operating System patches for Windows. More recently however, it has been expanded to include all Microsoft products and the name has changed to Microsoft Update, allowing the automated patching of non-OS software such as Internet Explorer and Microsoft Office.
 
​It is important to keep your machine up-to-date, but Windows Update Automatic installation can be somewhat intrusive to your work flow. There is nothing worse than getting Windows Updates installing during important presentation. You should set Windows Updates to be installed manually.

Go to     **Control Panel | Windows Update | Change Settings **and set updates to     **Download updates but let me choose whether to install them**.
![](/PublishingImages/win-update-1.jpg)Figure: Bad example – Install updates automatically![](/PublishingImages/win-update-2.jpg)Figure: Good example – Download updates but let user choose whether to install them
If you have a system administrator who manages your organization’s infrastructure, it is recommended to get you system administrator to push this setting via group policy.
![](/PublishingImages/win-update-3.jpg)Figure: Better example – Windows Updates setting is pushed to \*ALL\* users via group policy
