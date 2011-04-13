---
type: rule
title: Do you know how to setup your Outlook to send but not receive?
uri: do-you-know-how-to-setup-your-outlook-to-send-but-not-receive
created: 2011-04-13T06:18:47.0000000Z
authors:
- id: 21
  title: Matthew Hodgkins
- id: 1
  title: Adam Cogan

---

 When using your presentation computer you may want to still be able to send emails but not want to download your entire Exchange mailbox to your Boot2VHD image. This is especially relevant for people with large mailboxes.<br> 
1. Open Outlook 2010 and create a new Exchange account
2. Enter your server name and user name, but un-tick **Use Cached Exchange Mode
![Un-tick Use Cached Exchange Mode](/ITAndNetworking/RulesToBetterPresentationPCs/PublishingImages/fig3-untickcached.png)
**Figure - Un-tick Use Cached Exchange Mode
3. Finish the setup and then open Outlook
4. Configure your Send / Receive Groups:
![Click Send / Receive | Click Send / Receive Groups | Click Define Send / Receive Groups](/ITAndNetworking/RulesToBetterPresentationPCs/PublishingImages/fig4-editaccounts.png) Figure - Click Send / Receive | Click Send / Receive Groups | Click Define Send / Receive Groups
5. Now we can choose the parts of our mailbox we want to synced to our PC. The following options are recommened:

<br>    Untick **Receive Mail Items
**Tick **Download offline address book
**Tick the **Outbox** folder
<br>    Tick the **Contacts** folder
<br>    Tick the **Sent Items **folder, and select **Download headers only**

![](/ITAndNetworking/RulesToBetterPresentationPCs/PublishingImages/fig5-sendreciveall.png)
Figure - Untick "Receive mail items" | Tick "Sent Items", "Contacts" and "Outbox" | Download only headers for "Sent Items"
6. When back in the main Outlook window click **Send / Receive All** **Folders **and this will sync your sent items and contacts which will now be available offline


