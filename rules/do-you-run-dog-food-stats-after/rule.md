---
type: rule
title: Do you run Dog Food Stats (after)?
uri: do-you-run-dog-food-stats-after
created: 2009-11-08T02:01:52.0000000Z
authors: []

---


Running the "Dog Food" stats on your new TFS 2010 server is a good way to see if the upgrade was successful. You should check the new values against the [stats you noted down from your TFS 2008 server](/TFS/RulesToBetterTFS2010Migration/Pages/DogfoodStatsBefore.aspx).

1. On TFS2010, run the DogFoodStats queries on TFS2010 and save the results
<br>    ([http://blogs.msdn.com/granth/archive/2009/10/23/tfs2010-sql-queries-for-tfs-statistics.aspx](http&#58;//blogs.msdn.com/granth/archive/2009/10/23/tfs2010-sql-queries-for-tfs-statistics.aspx))
2. Compare the numbers are the same
    1. Note: Number will differ slightly (usually increases as TFS2010 checks in a few more items) 
<br>        Note: Grant Holiday as never published exactly why they ar not the same.



TFS2008:

===========================================

Files

-------- -----------

1        28052

2        335168

-- Compresed file size:

--------------------

11837952896




-- Uncompressed file sizes:

--------------------

24868196032

-- Areas & Iterations:

-----------

1096


Figure: Have a look at the dogfoodstats you ran before


TFS2010:

=============================================

Areas and Iterations

--------------------

1096




Files

-----------

347629




Compressed File Sizes

---------------------

11296




Uncompressed File Sizes

-----------------------

23723


Figure: You should get the same number or more for your TFS2010 server. We’re not worried unless it’s slightly less







 




