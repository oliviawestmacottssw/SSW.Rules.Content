---
type: rule
archivedreason: 
title: Do you turn off Database Mirroring before Upgrading your TFS databases?
guid: c8184551-e496-40dd-8109-0080909fbab5
uri: do-you-turn-off-database-mirroring-before-upgrading-your-tfs-databases
created: 2015-08-12T16:10:38.0000000Z
authors: []
related: []
redirects: []

---


<p>​To avoid headaches while upgrading the TFS database schemas, you should manually turn off database mirroring prior to running the Verify step of your configuration.</p>
<br><excerpt class='endintro'></excerpt><br>
<p><span style="line-height&#58;1.6;">If database mirroring is enabled on your TFS database, an additional step is required to temporarily turn it off when upgrading the database schema. This may require additional permissions that are difficult to check in the Verify step. Verification may hang with no sign of what's happening until you delve into the SQL Server logs. It's safer (and avoids problems) if you manually turn it off before you start.</span><br></p>


