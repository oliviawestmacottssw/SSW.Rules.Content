---
type: rule
archivedreason: 
title: Do you configure your TFS to be accessible from outside the network?
guid: c0ecaeb8-a15d-40aa-8617-b62004fe22ac
uri: do-you-configure-your-tfs-to-be-accessible-from-outside-the-network
created: 2011-11-18T03:53:00.0000000Z
authors:
- title: David Klein
  url: https://ssw.com.au/people/david-klein
- title: Justin King
  url: https://ssw.com.au/people/justin-king
- title: Ryan Tee
  url: https://ssw.com.au/people/ryan-tee
- title: Tristan Kurniawan
  url: https://ssw.com.au/people/tristan-kurniawan
related: []
redirects: []

---


<ul><li>TFS SP1&#160;<br>This feature called &quot;Extranet Support&quot; was added way back in TFS 2005 SP1 as per&#160;<a href="http&#58;//www.ssw.com.au/ssw/Redirect/StandardsRules/MSDNBlog.htm">Stuff in the pipe for Team Foundation Server</a>&#160;​</li><li>A domain name or IP address forwarded to TFS (eg&#58; tfs.your-domain.com)</li><li>Port 8080 (this is port that TFS uses for source control)</li><li>Firewall/Router rule (ideally)​</li></ul>
<br><excerpt class='endintro'></excerpt><br>
<p>Tip&#58; You can solve this with TFS Extranet Support&#58;</p> 
<p>Yes Port 8080 will work in most cases but not on the strictest networks, where only Port 80 is allowed. 
   <br>Then you have to use port forwarding via a firewall/router rule (recommended) to forward port 80 to the TFS port, while in this way, you would lose the TFS SharePoint Portal and Reporting Services. </p><dl><dt>
      <img alt="Rule to forward port 80 to the TFS port" src="/PublishingImages/tfs-firewall-rule-80.gif" width="681" height="339" />
   </dt><dd>Figure&#58; Rule to forward port 80 to the TFS port </dd></dl>


