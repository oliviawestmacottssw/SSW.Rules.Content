---
type: rule
title: Do you allow users to check for a new version easily?
uri: do-you-allow-users-to-check-for-a-new-version-easily
created: 2009-02-28T09:42:15.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

 This field should not be null (Remove me when you edit this field). 
Remember:

- This is mainly for Windows Forms, but you can do the same for new versions of Web Applications - e.g. a knowledge base package or Reporting Services Application.
- You can do a complete check of your PC at the click of a button using [SSW Diagnostics](http&#58;//www.ssw.com.au/ssw/Diagnostics/Default.aspx).
- Since this check occurs over the web, you should use [threading](http&#58;//www.ssw.com.au/ssw/Standards/Rules/RulesToBetterWindowsForms.aspx#GuiThreading) to avoid slowing down the forms responsiveness. This is a generic component that is available in the [SSW .NET Toolkit](http&#58;//www.ssw.com.au/ssw/NETToolkit/Default.aspx).
- If the UI is a Windows Service, be aware that they don't open up the UI very often. Therefore you can't rely on this method. In a coming release Diagnostics will ask for your email and let you know when updates are available for you PC.

![Check for Updates](/Standards/Management/RulesToSuccessfulProjects/PublishingImages/MSN.gif)Figure: BAD UI - a nagging message box that forces the User to click OK 
![ ](/Standards/Management/RulesToSuccessfulProjects/PublishingImages/GoodUI.gif) Figure: Show a Tick when the application is up to date 
![ ](/Standards/Management/RulesToSuccessfulProjects/PublishingImages/BadUI.gif) Figure: Show a Cross when the application is out of date 

To keep the consistent look and consistent code, we have implemented our version checker as a user control.
![ ](/Standards/Management/RulesToSuccessfulProjects/PublishingImages/VersionStatusControl.gif) Figure: SSW.Framework.WindowsUI.VersionStatus 
As it is a user control, we can easily implement this in all our applications. We just need to place the user control on the winform, and have the ProductDownloadID and ProductLatestVersionURL entered with the correct values.
![ ](/Standards/Management/RulesToSuccessfulProjects/PublishingImages/VersionStatusProperties.gif) Figure: Enter the ProductDownloadID and ProductLatestVersionURL   
![Check for Updates](/Standards/Management/RulesToSuccessfulProjects/PublishingImages/CheckForUpdate.gif)
Figure: Include 'Check for Updates' in your applications 
