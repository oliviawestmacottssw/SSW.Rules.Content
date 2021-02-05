---
type: rule
archivedreason: 
title: Do you run your dog food stats (before)?
guid: db69f69b-a073-4537-908d-52add92cac8a
uri: do-you-run-your-dog-food-stats-before1
created: 2015-08-12T16:38:41.0000000Z
authors: []
related: []
redirects:
- do-you-run-your-dog-food-stats-(before)1
- do-you-run-your-dog-food-stats-before
- do-you-run-your-dog-food-stats-(before)

---


<p>Run the excellent DogFoodStats queries&#58;</p><p>o&#160;&#160;&#160;For TFS 2010 - from Grant Holliday -&#160;<a href="http&#58;//blogs.msdn.com/b/granth/archive/2009/10/23/tfs2010-sql-queries-for-tfs-statistics.aspx">http&#58;//blogs.msdn.com/b/granth/archive/2009/10/23/tfs2010-sql-queries-for-tfs-statistics.aspx</a>&#160;&#160;&#160;.</p><p>o&#160;&#160;&#160;For TFS 2012 – update from Erin Dormier -<a href="http&#58;//blogs.msdn.com/b/visualstudioalm/archive/2013/08/20/tfs-internal-usage-statistics-1st-half-cy-2013.aspx%22%20%5cl%20%22comments">http&#58;//blogs.msdn.com/b/visualstudioalm/archive/2013/08/20/tfs-internal-usage-statistics-1st-half-cy-2013.aspx#comments</a>&#160;</p><div><br></div>
<br><excerpt class='endintro'></excerpt><br>
<p>While the above scripts are intended for older versions of TFS, many of the SELECT statements also work with TFS 2013 Update 4.</p><p>&#160;</p><p>The above scripts give you some great information about the details of our collections you can use for comparison afterwards.</p><p>Make sure you record these statistics so you can compare them after the upgrade.</p><p>Recent Users</p><p>------------</p><p>33</p><p>&#160;</p><p>Users with Assigned Work Items</p><p>------------------------------</p><p>145</p><p>Warning&#58; Null value is eliminated by an aggregate or other SET operation.</p><p>&#160;</p><p>Version Control Users</p><p>---------------------</p><p>244</p><p>&#160;</p><p>Total Work Items</p><p>----------------</p><p>20608</p><p>&#160;</p><p>Areas and Iterations</p><p>--------------------</p><p>1838</p><p>&#160;</p><p>Work Item Versions</p><p>------------------</p><p>93298</p><p>&#160;</p><p>Work Item Attachments</p><p>---------------------</p><p>11331</p><p>&#160;</p><p>Work Item Queries</p><p>-----------------</p><p>12768</p><p>&#160;</p><p>Files</p><p>-----------</p><p>694604</p><p>&#160;</p><p>Compressed File Sizes</p><p>---------------------</p><p>18042</p><p>&#160;</p><p>Uncompressed File Sizes</p><p>-----------------------</p><p>36315</p><p>&#160;</p><p>Checkins</p><p>-----------</p><p>53297</p><p>&#160;</p><p>Shelvesets</p><p>-----------</p><p>381</p><p>&#160;</p><p>Merge History</p><p>--------------------</p><p>846922</p><p>&#160;</p><p>Pending Changes</p><p>---------------</p><p>906</p><p>&#160;</p><p>Workspaces</p><p>-----------</p><p>259</p><p>&#160;</p><p>Local Copies</p><p>--------------------</p><p>4197458</p><p>&#160;</p><p>Command Execution Count</p><p>------------------------</p><p>Checkin&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160; 27</p><p>Get&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160; 578</p><p>Shelve&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160; 96</p><p>Upload&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160; 162</p><p>VCDownloadHandler&#160;&#160;&#160;&#160; 1403</p><p>GetWorkItem&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160; 558</p><p>QueryWorkitems&#160;&#160;&#160;&#160;&#160;&#160;&#160; 830</p><p>Update&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160; 272</p><p><strong>Figure&#58; Example result of DogFoodStats on our TFS 2010 instance</strong></p>


