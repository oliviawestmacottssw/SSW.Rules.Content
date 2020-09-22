---
type: rule
title: Do you know how to remove old Boot to VHD entries?
uri: do-you-know-how-to-remove-old-boot-to-vhd-entries
created: 2011-04-13T06:49:09.0000000Z
authors:
- id: 21
  title: Matthew Hodgkins

---

 When you have finished with the VHD for the presentation you will want to remove the boot entries that were created for the VHD.<br> 
1. Open an administrative command prompt
2. View all the boot entries by typing: bcdedit ![The list Boot entries after running bcdedit](fig6-listbootentries.png)
Figure - The list Boot entries after running bcdedit
3. Using the **identifier** from the previous step you can now run the following command to delete the entry:
bcdedit /delete **{identifier}**![The boot entry has now been deleted](fig7-deletingthebootentry.png)
Figure - The boot entry has now been deleted

 You can now delete or move your VHD file and you will not get any errors when booting your laptop.   
