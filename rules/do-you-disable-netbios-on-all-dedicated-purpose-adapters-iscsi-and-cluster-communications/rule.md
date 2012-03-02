---
type: rule
title: Do you disable NetBIOS on all dedicated purpose adapters (iSCSI and Cluster Communications)?
uri: do-you-disable-netbios-on-all-dedicated-purpose-adapters-iscsi-and-cluster-communications
created: 2012-03-02T19:44:44.0000000Z
authors: []

---

 To improve performance, it's a good idea to disable NetBIOS over TCP/IP on your cluster NIC and iSCSI NIC. NetBIOS isn't used in Server 2008 R2 clusters. ![Disable netBIOS](/ITAndNetworking/Rules-to-Better-Hyper-V-Clustering/PublishingImages/disable-netbios.jpg)Figure: Good example – the NetBIOS is disabled on the dedicated NIC's (iSCSI & Cluster Communications)
