---
type: rule
title: Do you know the best way to give the best customer support?
uri: do-you-know-the-best-way-to-give-the-best-customer-support
created: 2009-03-04T06:49:46.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

 There are a few methods to control a client's machine remotely, all of them have the same functionality, but different usage, and different pros and cons. <br> 
**Servers**

For server machines, we recommend using either Windows' built-in Remote Desktop (also knows as "Terminal Services" ) or a VNC-based tool. Remote Desktop provides each authenticated user a Windows logon session that is not shared. If your client lives in a place where the time zone is different, Remote Desktop should be your first choice as it doesn't need the client's interaction once Remote Desktop is enabled (typically it should have been enabled for a server for the ease for remote maintenance and monitoring).
![ ](/Management/RulesToSuccessfulProjects/SiteAssets/Pages/RemoteSupport/remoteconnection.png) Figure: Enabled Remote Desktop 
Remote Desktop works for workstations, but it's not recommended due to a security risk if Remote Support isn't disabled. Also, because of the End User License Agreement (EULA), only allows 1 user at a time, if you logon to client's Windows machine, the client will be logged off.

Of course the second option is a VNC-based remote tool, one of the main difference of a VNC-based remote tool is it shares the same logon session with the user who is currently logged on the machine. The server administrator doesn't need to give the user Windows' username and password, nor create a temporary user account. And because of both parties will share the same logon session, we see what the clients see, and so do they. Some clients may prefer this as they know what's happening exactly, which is important for a server. 
 The VNC tools we prefer: [TightVNC](http&#58;//www.ssw.com.au/ssw/Redirect/tightvnc.htm) and [UltraVNC](http&#58;//www.ssw.com.au/ssw/Redirect/ultravnc.htm).

**Desktop support**

For supporting end users' workstation machines remotely, here is the order you should try with the end users:

- [TeamViewer](http&#58;//www.ssw.com.au/ssw/Standards/Support/RemoteSupportViaTeamViewer.aspx) It’s easy, simple and works in most environments.
- [Skype​](http&#58;//www.skype.com/)
- [Lync](http&#58;//products.office.com/en/lync/lync)
- [Mikogo](https&#58;//www.mikogo.com/) (Free)
- [JoinMe](https&#58;//www.join.me/) (Free)
- [UltraVNC](http&#58;//www.ssw.com.au/ssw/Standards/Support/RemoteSupportViaUltraVNC.aspx) (Free)
- [Copilot](http&#58;//www.ssw.com.au/ssw/Standards/Support/RemoteSupportViaCopilot.aspx) The final option is to try Copilot - there is no screwing with firewalls at both sides. (Not free)​


The best way to handle a support call - ​[SSW Remote Support Standard](http&#58;//www.ssw.com.au/ssw/Standards/Support/RemoteSupportSampleScript.aspx)

See useful tools [The Best 3rd Party Network Tools - TeamViewer](http&#58;//www.ssw.com.au/ssw/Standards/DeveloperGeneral/networkTools.aspx#TeamViewer).

