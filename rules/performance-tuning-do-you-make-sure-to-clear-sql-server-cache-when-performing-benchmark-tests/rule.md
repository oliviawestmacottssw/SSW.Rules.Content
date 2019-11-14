---
type: rule
archivedreason: 
title: Performance Tuning - Do you make sure to clear SQL server cache when performing benchmark tests?
guid: e63b4ecc-b474-48a4-be95-9a777980bd36
uri: performance-tuning-do-you-make-sure-to-clear-sql-server-cache-when-performing-benchmark-tests
created: 2019-11-14T23:15:10.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
related: []
redirects: []

---


<p>When you are tuning SQL statements you tend to play in SQL management studio for a while. During this time SQL caches your query's and execution plans.<br>All well and good but when you are trying to speed up a existing query that is taking some time then you may not be making a difference even though your execution times are way down.</p><p>You really need to clear SQL's cache (or buffer) every time you test the speed of a query. This prevents the data and/or execution plans from being cached, thus corrupting the next test.</p><p>To clear SQL Server's cache, run&#160;<strong>DBCC DROPCLEANBUFFERS</strong>, which clears all data from the cache. Then run&#160;<strong>DBCC FREEPROCCACHE</strong>, which clears the stored procedure cache.​<br></p>
<br><excerpt class='endintro'></excerpt><br>
<dl class="image"><dt>​​<img src="/PublishingImages/ClearSQLServerCache_BenchmarkTests.jpeg" alt="ClearSQLServerCache_BenchmarkTests.jpeg" style="width&#58;750px;" /></dt><dd>Figure&#58; First call is after clearing the cache. The second one is without clearing the cache. (26 seconds vs 2 seconds)</dd></dl>


