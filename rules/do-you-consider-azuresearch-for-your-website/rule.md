---
type: rule
title: Do you consider AzureSearch for your website?
uri: do-you-consider-azuresearch-for-your-website
created: 2015-04-27T01:23:12.0000000Z
authors: []

---

 
AzureSearch is designed to work with Azure based data and runs on ElasticSearch. You may resist to choose this new service from the missing advanced search features and what seems to be an expensive monthly fee ($250 as of today). If so, follow this rule:

Consider AzureSearch if your Azure website:

1. Uses SQL Azure (or other Azure based data such as DocumentDB), and
2. Does not require advanced search features.


Keep in mind that 1) hosting of a full-text search service (such as ElasticSearch) will cost you labour for setting up and maintaining the infrastructure, and 2) a single Azure VM can cost you up to $450. Do not drop AzureSearch unless the missing features are absolutely necessary.
 


​ ​​​

![Untitled2.png](/SoftwareDevelopment/Rules-to-Better-Azure/SiteAssets/Pages/Consider-AzureSearch-for-your-Azure-website/Untitled2.png)
 Figure: Good Example - Azure website using AzureSearch for what it can deliver today 


​​​​![Untitled.png](/SoftwareDevelopment/Rules-to-Better-Azure/SiteAssets/Pages/Consider-AzureSearch-for-your-Azure-website/Untitled.png)
Figure: Bad Example - Azure website using ElasticSearch for a simple search that AzureSearch can do
