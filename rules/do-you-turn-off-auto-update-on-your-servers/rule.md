---
type: rule
archivedreason: https://rules.ssw.com.au/do-you-turn-off-auto-update-on-your-servers
title: Do you turn off auto update on your servers?
guid: 31e1abd1-5623-4f55-a31e-0ff068ae0084
uri: do-you-turn-off-auto-update-on-your-servers
created: 2010-06-24T01:43:02.0000000Z
authors:
- title: John Liu
  url: https://ssw.com.au/people/john-liu
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
related: []
redirects: []

---


A recent Security Hotfix has broken SharePoint WSS3 stand-alone installations.&#160; This has prompted Microsoft SharePoint team to quickly release information regarding how to fix the issue&#58;&#160;<a href="https&#58;//blogs.msdn.microsoft.com/sharepoint/2010/06/22/installing-kb938444/">https&#58;//blogs.msdn.microsoft.com/sharepoint/2010/06/22/installing-kb938444/​</a><br>
<br>
This again reminds us that it is always not a good idea to have Windows Update automatically updating your servers.&#160; There are a few reasons. 

<br><excerpt class='endintro'></excerpt><br>

  
<ol>
    <li>​The previously mentioned problem - where the hotfix could bring down a production environment.&#160; <br></li>
    <li>In fact, even in a development environment this could be hours of lost work as the development team struggles to understand why only <strong>some</strong> of the developers' SharePoint <strong>magically and mysteriously </strong>broke overnight.</li>
    <li>Windows Update could restart your server, or put your server in a state where it requires restarting - preventing any urgent MSI installs without bringing down the server.</li>
</ol>
<p>Windows Update remains the best thing for end-users to protect their systems.&#160; But in a server, especially a production server environment - Windows Update patches are just like any new versions of the software that's built internally.&#160; It should be tested and then deployed in a controlled manner.<br>
<br>So recommendations&#58;</p>
<ol>
    <li>Windows Updates may be critical and should be kept relatively up to date.</li>
    <li>Have a plan where your awesome Network Admins schedule time to keep the servers up to date - including testing that the servers still perform its functions.</li>
    <li>Turn off Automatic Windows Update on Windows Servers</li>
</ol>



