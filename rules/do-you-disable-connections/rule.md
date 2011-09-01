---
type: rule
title: Do you disable connections?
uri: do-you-disable-connections
created: 2009-11-03T21:28:04.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 3
  title: Eric Phan

---


Once you are ready to start you need to make sure that no one can access the existing TFS 2008 server while you do the migration.

1. You are ready to start
2. Send out an email notifying all users that TFS2008 will be turned off. 
<br>    Follow [Rules to better Networks](http&#58;//www.ssw.com.au/SSW/Standards/Rules/RulesToBetterNetworks.aspx#rebootrestart)
3. Make sure no-one can check in files by either:
    1. Runinng [TFSQuiesce](http&#58;//support.microsoft.com/kb/950893) (recommended) 
<br>        or
    2. Turning off TFS Service
        1. Remote desktop into TFS 2008
        2. Start IIS
        3. Right click Team Foundation Server | Stop

![](/TFS/RulesToBetterTFS2010Migration/PublishingImages/StopTFSServices.png)
Figure: You need to stop anyone checking in files
4. Confirm you can no longer get latest on the Northwind team project


