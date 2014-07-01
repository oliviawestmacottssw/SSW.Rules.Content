---
type: rule
title: Do you know how to troubleshoot Lync connectivity or configuration issues?
uri: do-you-know-how-to-troubleshoot-lync-connectivity-or-configuration-issues
created: 2012-04-17T21:06:54.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

 At times especially during the initial implementation you may encounter some issues with Lync. The following are some of the useful tools which will assist you in identifying were the problem lies. 
Remote UC Troubleshooting Tool (RUCT) for Lync will show that the DNS records used by the Lync mobility clients to auto-discover the Lync mobility service have been added. This tool can be acquired from     [Inside OCS blog](http&#58;//insideocs.com/).

Specifically you now have the option of querying the locally configured DNS server for the following records:

- Lyncdiscover. (both CNAME or A record)
- Lyncdiscoverinternal. (both CNAME or A record)
- From the same screen you can ping the resulting hostname or test the port availability on any of the Lync DNS record matches

![Lync Auto-discovery](/PublishingImages/lync-auto-discovery.jpg) Figure: Lync Auto-Discovery Mobility DNS record
### Lync Monitoring Reports

The Monitoring Server collects data from the call detail recording (CDR) and Quality of Experience (QoE) databases and presents that data with the help of the SQL Server Reporting Services and the predefined Monitoring reports. These reports will show statistics which will assist in identifying issues such as network issues such as latency and packet loss.

### Internet Network connectivity tests

Tools such as     [Pingtest.net](http&#58;//pingtest.net/) and VisualRoute 2010 will assist in highlight problems related latency and packet loss.
![VisualRoute 2010 tool](/PublishingImages/visualroute-tool.jpg) Figure: VisualRoute 2010 tool showing a test to a Google DNS server
Read more about     [​implementing Microsoft Lync](http&#58;//www.ssw.com.au/ssw/Consulting/Lync.aspx).
​  
