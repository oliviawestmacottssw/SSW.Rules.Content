---
type: rule
title: Do you snapshot Virtual Machines before big changes?
uri: do-you-snapshot-virtual-machines-before-big-changes
created: 2011-02-14T06:18:58.0000000Z
authors:
- id: 21
  title: Matthew Hodgkins

---


Snapshots are a very convent way to back up a system before a big change is made. It is important to note that Microsoft does not support snapshots of running systems. This is because a snapshot is taken of the system exactly as is, with open connections and interrupt requests. For more information on this you can read Brian Harry’s blog post here: [http://blogs.msdn.com/bharry/archive/2010/02/10/a-tfs-2010-upgrade-success-story.aspx](http&#58;//blogs.msdn.com/bharry/archive/2010/02/10/a-tfs-2010-upgrade-success-story.aspx)

This is why you **MUST **shut down your server before taking a snapshot.

1. Shutdown the virtual server
2. In the **Hyper-V Manager**, ensure the Virtual Machine has the state of **Off**
3. Right click on the virtual machine you wish to snapshot and click **Snapshot**
4. The snapshot should run very quickly and you will notice the snapshot in the **Snapshots **area of the **Hyper-V Manager

![You will see the snapshots associated with a Virtual Machine when you click on them](/PublishingImages/snapshot-while-off.jpg)**
**You will see the snapshots associated with a Virtual Machine when you click on them
**
5. You can start your server back up again


