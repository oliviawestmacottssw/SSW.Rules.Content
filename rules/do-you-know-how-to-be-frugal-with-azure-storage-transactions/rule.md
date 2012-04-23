---
type: rule
archivedreason: 
title: Do you know how to be frugal with Azure Storage Transactions?
guid: 38ac2eba-4663-4e86-afb0-6bee2847d994
uri: do-you-know-how-to-be-frugal-with-azure-storage-transactions
created: 2012-04-23T14:23:33.0000000Z
authors:
- title: Adam Stephensen
  url: https://ssw.com.au/people/adam-stephensen
related: []
redirects: []

---


Azure transactions are CHEAP. You get tens of thousands for just a few cents. What is dangerous though is that it is very easy to have your application generate hundreds of thousands of transactions a day.
<br><excerpt class='endintro'></excerpt><br>
<p>Every call to Windows Azure Blobs, Tables and Queues count as 1 transaction. Windows Azure diagnostic logs, performance counters, trace statements and IIS logs are written to Table Storage or Blob Storage.</p>
<p>If you are unaware of this, it can quickly add up and either burn through your free trial account, or even create a large unexpected bill.</p>
<p><strong>Note&#58;</strong> Azure Storage Transactions do not count calls to SQL Azure.</p>
<h2>Ensure that Diagnostics are Disabled for your web and worker roles</h2>
<p>Having Diagnostics enabled can contribute 25 transactions per minute, this is 36,000 transactions per day.</p>
<p>Question for Microsoft&#58; Is this per Web Role?</p>

<img class="ms-rteCustom-ImageArea" alt="Check properties" src="/SoftwareDevelopment/Rules-to-Better-Azure/PublishingImages/azure-check-properties.jpg" />
<span class="ms-rteCustom-FigureNormal">Figure&#58; Check the properties of your web and worker role configuration files</span>

<img class="ms-rteCustom-ImageArea" alt="Disable Diagnostics" src="/SoftwareDevelopment/Rules-to-Better-Azure/PublishingImages/azure-disable-diagnostics.jpg" />
<span class="ms-rteCustom-FigureNormal">Figure&#58; Disable diagnostics</span>

<h2>Disable IntelliTrace and Profiling</h2>

<img class="ms-rteCustom-ImageArea" alt="Azure publishing settings" src="/SoftwareDevelopment/Rules-to-Better-Azure/PublishingImages/azure-publishing-settings.jpg" />
<span class="ms-rteCustom-FigureNormal">Figure&#58; When publishing, ensure that IntelliTrace and Profiling are both disabled</span>

<h2>Robots.txt </h2>
<p>Search bots crawling your site to index it will lead to a lot of transactions. Especially for web &quot;applications&quot; that do not need to be searchable, use Robot.txt to save transactions.</p>

<img class="ms-rteCustom-ImageArea" alt="Place robots.txt" src="/SoftwareDevelopment/Rules-to-Better-Azure/PublishingImages/azure-robots.jpg" />
<span class="ms-rteCustom-FigureNormal">Figure&#58; Place robots.txt in the root of your site to control search engine indexing</span>

<h2>Continuous Deployment</h2>
<p>When deploying to Azure, the deployment package is loaded into the Storage Account. This will also contribute to the transaction count.</p>
<p>If you have enabled continuous deployment to Azure, you will need to monitor your transaction usage carefully.</p>

<h3>References</h3>
<ul>

<li><a href="http&#58;//blogs.msdn.com/b/windowsazurestorage/archive/2010/07/09/understanding-windows-azure-storage-billing-bandwidth-transactions-and-capacity.aspx%20target=">Understanding Windows Azure Storage Billing – Bandwidth, Transactions, and Capacity</a></li>
<li><a href="http&#58;//serverfault.com/questions/363803/does-windows-azure-hosted-service-use-storage-transactions%20target=">Does Windows Azure hosted service use storage transactions</a></li>
</ul>






