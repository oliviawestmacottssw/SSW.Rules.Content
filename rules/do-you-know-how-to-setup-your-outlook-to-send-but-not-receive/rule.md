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

 When using your presentation computer you may want to still be able to send emails but not want to download your entire Exchange mailbox to your Boot2VHD image. This is especially relevant for people with large mailboxes. <br> 
Here is how you do it:

1. Open Outlook and create a new Exchange account: <br>      
![Create New Account](mail1.png)Figure - Tick manually configure server settings
2. ​Enter your server name and user name, but un-tick <br>      **Use Cached Exchange Mode**: ​ <br>      ![Un-tick Use Cached Exchange Mode](Mail3.png)Figure - Un-tick Use Cached Exchange Mode
3. Finish the setup and then open Outlook
4. Configure your Send / Receive Groups: <br>      ![Click Send / Receive | Click Send / Receive Groups | Click Define Send / Receive Groups](Email2.png)Figure - Click Send / Receive | Click Send / Receive Groups | Click Define Send / Receive Groups
5. Now we can choose the parts of our mailbox we want to synced to our PC. The following options are recommended:
    - Untick <br>            **Receive Mail Items**
    - Tick <br>            **Download offline address book**
    - Tick the <br>            **Outbox** folder
    - Tick the <br>            **Contacts** folder
    - Tick the <br>            **Sent Items **folder,
    - and select <br>            **Download headers only**

![](Email.png)Figure - Untick "Receive mail items" | Tick "Sent Items", "Contacts" and "Outbox" | Download only headers for "Sent Items"
6. When back in the main Outlook window click <br>      **Send / Receive ****All****Folders **and this will sync your sent items and contacts which will now be available offline


**Suggestion to the Microsoft Outlook Team:**

- ​Give us a "Sync last x weeks" for each folder
- Give us a "Work in Minimal Mode"​ that does the above


