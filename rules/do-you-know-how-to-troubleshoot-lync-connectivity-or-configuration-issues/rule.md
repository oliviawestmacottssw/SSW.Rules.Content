---
type: rule
archivedreason: 
title: Do you know how to troubleshoot Lync connectivity or configuration issues?
guid: 3e50c914-d83f-41fa-b70d-f0d6fd34935d
uri: do-you-know-how-to-troubleshoot-lync-connectivity-or-configuration-issues
created: 2012-04-17T21:06:54.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
related: []
redirects: []

---


At times especially during the initial implementation you may encounter some issues with Lync. The following are some of the useful tools which will assist you in identifying were the problem lies.
<br><excerpt class='endintro'></excerpt><br>
<p>Remote UC Troubleshooting Tool (RUCT) for Lync will show that the DNS records used by the Lync mobility clients to auto-discover the Lync mobility service have been added. This tool can be acquired from <a target="_blank" href="http&#58;//insideocs.com/">Inside OCS blog</a>.</p>
<p>Specifically you now have the option of querying the locally configured DNS server for the following records&#58;</p>
<ul>
<li>Lyncdiscover. (both CNAME or A record)</li>
<li>Lyncdiscoverinternal. (both CNAME or A record)</li>
<li>From the same screen you can ping the resulting hostname or test the port availability on any of the Lync DNS record matches</li>
</ul>
<img class="ms-rteCustom-ImageArea" alt="Lync Auto-discovery" src="/ITAndNetworking/PublishingImages/lync-auto-discovery.jpg" />
<span class="ms-rteCustom-FigureNormal">Figure&#58; Lync Auto-Discovery Mobility DNS record</span>
<h2>Lync Monitoring Reports</h2>
<p>The Monitoring Server collects data from the call detail recording (CDR) and Quality of Experience (QoE) databases and presents that data with the help of the SQL Server Reporting Services and the predefined Monitoring reports. These reports will show statistics which will assist in identifying issues such as network issues such as latency and packet loss.</p>
<h2>Internet Network connectivity tests</h2>
<p>Tools such as <a target="_blank" href="http&#58;//pingtest.net/">Pingtest.net</a> and VisualRoute 2010 will assist in highlight problems related latency and packet loss.</p>
<img class="ms-rteCustom-ImageArea" alt="VisualRoute 2010 tool" src="/ITAndNetworking/PublishingImages/visualroute-tool.jpg" />
<span class="ms-rteCustom-FigureNormal">Figure&#58; VisualRoute 2010 tool showing a test to a Google DNS server</span>



