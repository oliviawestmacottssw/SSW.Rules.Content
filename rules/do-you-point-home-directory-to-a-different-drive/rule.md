---
type: rule
title: Do you point Home directory to a different drive?
uri: do-you-point-home-directory-to-a-different-drive
created: 2016-05-30T06:23:41.0000000Z
authors:
- id: 46
  title: Danijel Malik

---

When you run Octopus Deploy setup the application installs to you %Program Files%\Octopus Deploy folder. If you installed Octopus Server you will see Server subfolder and if you installed Octopus Tentacle then it will be Tentacle. However, this is a folder where Octopus Deploy bits live, not your applications, packages, etc. Those artifacts live in the Home folder that you specify during the Octopus Setup Wizard the first time you configure the Server/Tentacle.
   By default the Home directory points to %SystemDrive%\Octopus which is not great. The main reason is that the Home folder is constantly growing and clogging up your OS drive. So you need to point the Home folder to a new drive e.g. D:\Octopus



![2016-05-30_12-18-02.png](2016-05-30_12-18-02.png)

Bad<br>Example - Home directory is pointing to %SystemDrive%



![2016-05-30_12-29-09.png](2016-05-30_12-29-09.png)

Good Example - Home directory is pointing to another drive
