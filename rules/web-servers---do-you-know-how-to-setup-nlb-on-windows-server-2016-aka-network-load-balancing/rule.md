---
type: rule
title: Web Servers - Do you know how to Setup NLB on Windows Server 2016? (aka Network Load Balancing)
uri: web-servers---do-you-know-how-to-setup-nlb-on-windows-server-2016-aka-network-load-balancing
created: 2011-11-14T15:08:00.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 21
  title: Matthew Hodgkins

---

 
Downtime occurs when you have a single server setup.

Use NLB to allow load balancing and failover. On each of your Windows Servers you will host your website.

You need to follow these steps to get it up and running:
 
1. On all nodes of the NBL cluster, the Network Load Balancing Feature needs to be installed.
![Setup NLB](/PublishingImages/Setup-NLB-1.jpg) Figure: Install the NLB Feature
2. Open the Network Load Balancing Manager from Administrative Tools
![Setup NLB](/PublishingImages/Setup-NLB-2.jpg) Figure: Under the Cluster menu item, click New
3. Enter the first node in the cluster in ‘Host’ and press ‘Connect’
![Setup NLB](/PublishingImages/Setup-NLB-3.jpg) Figure: Select the interface for the node
4. Enter a Priority as 1 (this is just a host identifier)
![Setup NLB](/PublishingImages/Setup-NLB-4.jpg) Figure: In 'Priority' enter '1'
5. ![Setup NLB](/PublishingImages/Setup-NLB-5.jpg) Figure: Enter a virtual IP address for the cluster. eg. 192.168.1.12
6. Choose the IP address of your cluster from the dropdown list Set a Full Internet Name eg. spcluster.sydney.ssw.com.au. 
Ensure the Multicast Cluster operation mode is selected.
![Setup NLB](/PublishingImages/Setup-NLB-6.jpg) Figure: Set the 3 cluster parameters
7. You want sticky sessions so you don’t mistakenly bounce between servers (and lose your state)
![Setup NLB](/PublishingImages/Setup-NLB-7.jpg) Figure: Leave the Port Rule as default. This will provide sticky sessions
![Setup NLB](/PublishingImages/Setup-NLB-8.jpg) Figure: Success. The cluster configuration will show a green icon
8. Right click the name of the cluster eg. spcluster.sydney.ssw.com.au Click Add Host To Cluster
![Setup NLB](/PublishingImages/Setup-NLB-9.jpg) Figure: Add the 2nd web server
9. Enter the host name of the next node eg. SYDVMAPS2010P02
Click connect
![Setup NLB](/PublishingImages/Setup-NLB-10.jpg) Figure: Enter the 2nd web servers name
10. Take the default settings, assuring the ‘Priority (unique host identifier)’ is different than the first node:
![Setup NLB](/PublishingImages/Setup-NLB-1.jpg) Figure: Set the priority as #2
11. Take defaults on Port Rules page and click Finish
12. Success. The status of the cluster will now be Converged
![Setup NLB](/PublishingImages/Setup-NLB-12.jpg) Figure: Success with 2 green icons
13. Open a command prompt and type in wlbs query to verify the cluster:
![Setup NLB](/PublishingImages/Setup-NLB-13.jpg) Figure: Type in wlbs query to verify the cluster
14. Ping both nodes and the virtual IP address externally to verify they are all working


