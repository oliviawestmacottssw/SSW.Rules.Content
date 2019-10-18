---
type: rule
archivedreason: 
title: Do you manage Virtual Machines through Virtual Machine Manager (VMM)?
guid: 8e37f938-704d-42d0-818a-ff4018d1c856
uri: do-you-manage-virtual-machines-through-virtual-machine-manager-vmm
created: 2019-10-18T00:15:26.0000000Z
authors: []
related: []
redirects: []

---


<div>Virtual Machine Manager (VMM) is made for managing Virtual Machines (VM)!</div>Everything is easy to set up and deploy using VMM.<br>
<br><excerpt class='endintro'></excerpt><br>
<p>​You can provision VMs using a number of different approaches in VMM&#58;</p><p>&#160; 1. <a href="https&#58;//docs.microsoft.com/en-us/system-center/vmm/vm-blank-disk?view=sc-vmm-2019">Create VMs from a blank virtual disk</a>;<br>&#160; 2. <a href="https&#58;//docs.microsoft.com/en-us/system-center/vmm/vm-existing-disk?view=sc-vmm-2019">Create VMs from existing hard disks</a>;<br>&#160; 3. <a href="https&#58;//docs.microsoft.com/en-us/system-center/vmm/vm-clone?view=sc-vmm-2019">Clone a VM from existing VM</a>;<br>&#160; 4. <a href="https&#58;//docs.microsoft.com/en-us/system-center/vmm/vm-template?view=sc-vmm-2019">Create VM from a template</a>;<br>&#160; 5. Create VM in a service deployment;<br>&#160; 6. <a href="https&#58;//docs.microsoft.com/en-us/system-center/vmm/vm-san-copy?view=sc-vmm-2019">Rapidly provision a VM using storage area network (SAN) copy</a>.</p><p>You can also deploy VM guest clusters that acts as a failover cluster for your VMs, sharing the same .vhdx files as the main ones!</p><p>VMM uses an algorithm to intelligently place your newly created virtual machine on an available host, depending on a few factors&#58;</p><p>&#160; 1. CPU rating;<br>&#160; 2. RAM rating;<br>&#160; 3. Disk I/O rating;<br>&#160; 4. Network rating.</p><p>It then places the VM in the best host available for it.</p><p>VMM does this and much more for VMs, and you can read a bigger explanation <a href="https&#58;//docs.microsoft.com/en-us/system-center/vmm/provision-vms?view=sc-vmm-2019">here</a>.<br></p>


