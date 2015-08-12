---
type: rule
title: Do you disable connections?
uri: do-you-disable-connections
created: 2015-08-12T15:42:01.0000000Z
authors: []

---

 
It is important that while you're upgrading, nobody can check in.  Any check-ins after you backup your database will be lost.

To make sure that nobody can change anything during the upgrade, follow these steps.
 
a.               Send out an email notifying everyone TFS will be unavailable for the upgrade period
 Follow [Rules to better Networks](http&#58;//www.ssw.com.au/SSW/Standards/Rules/RulesToBetterNetworks.aspx#rebootrestart)

b.              Make sure nobody can check in files:

.                Open the TFS Administration Console on the server.

a.               Navigate to Application Tier / Team Project Collections.

b.              For each Team Project Collection, select it, and click "Stop Collection". Enter a useful message (this will be displayed to users trying to connect from Visual Studio) and click "Stop":

![stop each term.png](/SiteAssets/do-you-disable-connections-1/stop%20each%20term.png)

**Figure: Stop each Team Project Collection**



![all team project.png](/SiteAssets/do-you-disable-connections-1/all%20team%20project.png)

**Figure: All Team Project Collections are stopped**

c.               In Visual Studio, confirm you can no longer connect to TFS



![visual studio.png](/SiteAssets/do-you-disable-connections-1/visual%20studio.png)

**Figure: Visual Studio shows the message that you entered when you stopped the Team Project Collection**

