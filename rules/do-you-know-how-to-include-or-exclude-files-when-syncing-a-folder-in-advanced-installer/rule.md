---
type: rule
title: Do you know how to include or exclude files when syncing a folder in Advanced Installer?
uri: do-you-know-how-to-include-or-exclude-files-when-syncing-a-folder-in-advanced-installer
created: 2014-09-18T20:30:43.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 46
  title: Danijel Malik

---

If you are syncing your Application Folder (or any other) with a local folder on a disk, you can specify which file or folders you want to sync. This is a very convenient way to keep your package smaller and clean.

Here is how you do it:
 
1. Right click the <br>      **Application Folder** and choose <br>      **Properties**
2. Click on Filters button to open the <br>      **Edit Filters** dialog
3. Click on <br>      **New** button to create Include pattern. Alternatively you can switch to <br>      **Exclude Filters** tab
4. Enter the Pattern and press <br>      **OK** on each screen


![ Edit Filters dialog](installers-include-exclude-1.jpg)

[[badExample]]
| ![ Bad Example - Synced folder contains files that are not supposed to be deployed](installers-include-exclude-2.jpg)

[[goodExample]]
| ![ Good Example - Synced folder is filtered so that it includes only files we want to deploy](installers-include-exclude-3.jpg)
