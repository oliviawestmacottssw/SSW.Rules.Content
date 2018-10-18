---
type: rule
archivedreason: 
title: Do you do organize your hard disk?
guid: 0b99ae80-634b-47db-9a7b-b6d3763361f3
uri: do-you-do-organize-your-hard-disk
created: 2018-06-04T02:06:32.0000000Z
authors:
- title: Kaique Biancatti
  url: https://ssw.com.au/people/kaique-biancatti
related: []
redirects: []

---


​Using a standard file structure for storing user data on laptops makes locating the important information fast and performing automated backup operations easy - Use this checklist&#58; <br>​<br>
<br><excerpt class='endintro'></excerpt><br>
<div><h3 class="ssw15-rteElement-H3">Domain-joined checklist&#58;<br></h3></div><p class="ssw15-rteElement-GreyBox">
   <strong>1. Is your computer domain-joined?</strong><br>If your computer is domain-joined, then your backup script should already be working daily at 11 am.&#160;<br>Go to&#160;\\fileserver.sydney.ssw.com.au\UserBackups\ztBackupScripts\UserLogs.log to see the last time your backup was done.&#160; 
   <br>
   <strong>Date last Run&#58; xxx&#160;</strong><br><br><strong>2. Was it run last week?</strong><br><br><strong>3. Did you manually run the Login script?</strong><br>If your computer is domain-joined, the Login Script should have run already when you logged in. Go to your C&#58;\ drive and look for SSWLoginScript.log. Open it and see the last time it was run.<br><strong>Date Last Run&#58; xxx</strong><br><br><strong>4.&#160;Was it run last week?</strong><br>​<br></p><h3 class="ssw15-rteElement-H3">​Non-domain-joined checklist&#58;<br></h3><div><p class="ssw15-rteElement-P">
      <b>1. Do you use a cloud backup application?</b></p><div><p class="ssw15-rteElement-P">Some good options include OneDrive for Business and Dropbox. You should always keep important files in the cloud for security reasons. You can read more about it 
         <a href="/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=68798bd6-a0fa-49ee-89ea-d4d0d11930f1">here</a>.<br></p><p class="ssw15-rteElement-P">
         <b>2. Which one?</b><br></p><p class="ssw15-rteElement-P">Read more about it&#160;here.<br></p><p class="ssw15-rteElement-P">
         <b>3. Has it run in the last week?</b><br></p><p class="ssw15-rteElement-P">
         <b>4.&#160;Do you gather important files in one folder structure?</b></p><p class="ssw15-rteElement-P">Create a folder named &quot;Data&lt;YourUserName&gt;&quot; and use it to store all important files that need to be backed up there. You can create new subfolders in it, but always use this one, as it makes it easier to see what needs to be backup up.<br></p><p class="ssw15-rteElement-P">Everything in this folder should be safely and securely backed up.<br></p><p class="ssw15-rteElement-P">Create a folder in C&#58; with Data and your username, for example,&#160;&quot;C&#58;\DataKaiqueBiancatti&quot;&#58;<br></p><dl class="image"><dt> 
            <img src="/PublishingImages/sswDataFolderExample.png" alt="sswDataFolderExample.png" /> 
         </dt><dd>Figure&#58; Location of&#160;<strong style="color&#58;#444444;">DataUsername&#160;</strong></dd></dl><p></p><p class="ssw15-rteElement-P">
         <strong></strong> 
         <span style="font-size&#58;1rem;font-weight&#58;bold;color&#58;#444444;">5. Do you know the size and location of your backup folder?&#160;</span></p><p class="ssw15-rteElement-P">You should always stick with the C&#58;\DataUsername location for your backups, and always keep it there. Also, do not forget that cloud services have limited storage space, so always check the size of your backup folder is not exceeding the amount of storage space you have.&#160;</p><p class="ssw15-rteElement-P">
         <strong style="font-size&#58;16px;">6. Where is it located now?<br></strong><br></p><p class="ssw15-rteElement-P">
         <span style="font-size&#58;16px;"> 
            <strong>7. Do you do your backups periodically and automatically?</strong><br><span style="font-size&#58;13px;">The beauty of using cloud backup solutions is the ability of it&#160;</span><span style="font-size&#58;13px;">synchronizing</span><span style="font-size&#58;13px;">&#160;your files automatically, keeping them safe for you, even if you forget about it. Check if your chosen application is backing up the &quot;C&#58;\DataYourUsername&quot; automatically.<br></span><br style="font-size&#58;13px;"></span><span style="font-size&#58;1rem;font-weight&#58;bold;color&#58;#444444;">8.&#160;Do you keep your Outlook PST/OST separated from your cloud backups?</span><span style="font-size&#58;16px;"><br></span></p><p>Outlook mailboxes tend to get huge in size pretty quickly, and your emails are already being backed up by your Exchange Server, so there is no need to back these&#160;files up. PST files (Outlook&#160;2013 and earlier) contain all your mailbox messages and&#160;OST files (Outlook 2016 and newer) contain all your messages to be used offline.<br></p><p>Create a folder in C&#58; named &quot;DataExchange&quot;&#160; for storing the MS Outlook file, not in the same place as your &quot;Data&quot; folder.<br></p><dl class="image"><dt> 
            <img src="/PublishingImages/ssw22.png" alt="ssw22.png" />
         </dt><dd>Figure&#58; Location of DataExchange </dd></dl><h3 class="ssw15-rteElement-H3">​Extra tips for organizing your hard drive&#58;<br></h3><ul class="ssw15-rteElement-P"><li>Create a temporary folder for temporary files, like &quot;C&#58;\temp&quot;. It makes it easier to see.<br></li><li>Keep a clean desktop, delete anything that is not necessary from there and does not save things there by default. Having a messy desktop just makes everything confusing.<br></li></ul></div>
   <br>
</div>


