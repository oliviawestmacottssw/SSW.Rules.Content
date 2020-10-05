---
type: rule
title: Do you manage Hyper-V Networks through Virtual Machine Manager (VMM)?
uri: do-you-manage-hyper-v-networks-through-virtual-machine-manager-vmm
created: 2019-10-17T23:09:31.0000000Z
authors:
- id: 73
  title: Kaique Biancatti

---

Virtual Machine Manager (VMM) lets you easily apply network settings to a Hyper-V host or cluster.
 
​Instead of managing each Virtual Machine network itself, using VMM to manage them all is much easier.

To do that, you need to complete a few steps:

1. Configure network settings with a logical switch;

You can learn more on how to set this up [here](https&#58;//docs.microsoft.com/en-us/system-center/vmm/network-switch?view=sc-vmm-2019).

  2. Ask yourself: "What is this network adapter going to be used for?"

You need to specify if the network adapter is going to be used for virtual machines, host management, etc...

3. Apply the logical switch and monitor physical network devices

For full instructions on how to do this, see [here](https&#58;//docs.microsoft.com/en-us/system-center/vmm/hyper-v-network?view=sc-vmm-2019).
