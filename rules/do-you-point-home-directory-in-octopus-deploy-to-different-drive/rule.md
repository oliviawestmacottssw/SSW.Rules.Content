---
type: rule
archivedreason: 
title: Do you point Home directory to a different drive?
guid: 00d65e16-be52-489d-b030-f03e9176e532
uri: do-you-point-home-directory-in-octopus-deploy-to-different-drive
created: 2016-05-30T06:23:41.0000000Z
authors:
- title: Danijel Malik
  url: https://ssw.com.au/people/danijel-malik
related: []
redirects:
- do-you-point-home-directory-to-a-different-drive

---


<p>​​​When you run Octopus Deploy setup the application installs to you %Program Files%\Octopus Deploy folder. If you installed Octopus Server you will see Server subfolder and if you installed Octopus Tentacle then it will be Tentacle. However, this is a folder where Octopus Deploy bits live, not your applications, packages, etc. Those artifacts live in the Home folder that you specify during the Octopus Setup Wizard the first time you configure the Server/Tentacle.​</p>
<br><excerpt class='endintro'></excerpt><br>
By default the Home directory points to %SystemDrive%\Octopus which is not great. The main reason is that the Home folder is constantly growing and clogging up your OS drive. So you need to point the Home folder to a new drive e.g. D:\Octopus<div><br></div><div><img src="2016-05-30_12-18-02.png" alt="2016-05-30_12-18-02.png" style="margin:5px;width:808px;" /><br><div><dd class="ssw15-rteElement-FigureBad">​​Bad
Example - Home directory is pointing to %SystemDrive%​​</dd><div><br></div><div><img src="2016-05-30_12-29-09.png" alt="2016-05-30_12-29-09.png" style="margin:5px;width:808px;" /><br></div><dd class="ssw15-rteElement-FigureGood">​​​Good Example - Home directory is pointing to another drive​</dd></div></div>


