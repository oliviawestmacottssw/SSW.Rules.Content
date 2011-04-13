---
type: rule
title: Do you know what features to install on a Windows Server VHD?
uri: do-you-know-what-features-to-install-on-a-windows-server-vhd
created: 2011-04-13T05:51:43.0000000Z
authors:
- id: 21
  title: Matthew Hodgkins

---

 When you setup a new Windows 2008 R2 VHD it will be lacking a few components that need to be installed so it can function as a personal computer as well as a presentation computer.<br> 
1. Open **Server Manager**
2. Click on **Add Features**
3. Install **Desktop Experience **and **Wireless LAN Service**


If you want to enable themes:

1. Open **services.msc **and **Enable **the **Themes **service
2. Then go to the** Start Menu **and type **Adjust the appearance and performance of Windows**
3. Put the radio button in **Adjust for best performance**


