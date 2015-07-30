---
type: rule
title: Do you know how to convert Dynamics CRM managed solution to unmanaged
uri: do-you-know-how-to-convert-dynamics-crm-managed-solution-to-unmanaged
created: 2015-06-18T04:36:23.0000000Z
authors: []

---

 You might need to modify solutions during migration. But if that solution is managed, you cannot edit directly. If you have the unmanaged version in development environment, you can edit it and override the production managed solution. 
If you don't have the unmanaged version which is bad practice. see [her​e](http&#58;//community.adxstudio.com/blogs/shan/2014-01-17-converting-crm-solutions-from-managed-to-unmanaged/) for good practice about CRM ALM (How to avoid this section), use the following script to hack the org database


| ​<br>declare @solutionId uniqueidentifier, @systemSolutionId uniqueidentifier<br> <br>-- specify the uniquename of the managed solution you'd like to unmanage here it is StagingOrg<br> <br>select @solutionId = solutionid from SolutionBase where UniqueName='Your solution name'<br> <br>-- DO NOT TOUCH FROM HERE ON --<br> <br>select @systemSolutionId = solutionid from SolutionBase where UniqueName='Active'<br> <br>update PublisherBase set IsReadonly=0<br> <br>where PublisherId in (select PublisherId from SolutionBase where SolutionId=@solutionId)<br> <br>print 'updated publisher'<br>  <br>declare @tables table (id int identity, name nvarchar(100), ismanaged bit, issolution bit)<br> <br>declare @count int, @currentTable nvarchar(100), @currentM bit, @currentS bit, @sql nvarchar(max)<br> <br>-- go through all the tables that have the ismanaged/solutionid flag, find the related records for the current solution and move them to the crm active solution.<br> <br>insert into @tables (name, ismanaged, issolution)<br> <br>select name, 1, 0 from sysobjects where id in<br> <br>(select id from syscolumns where name in ('IsManaged'))<br> <br>and type='U'<br> <br>order by name<br> <br><br> <br>insert into @tables (name, ismanaged, issolution)<br> <br>select name, 0, 1 from sysobjects where id in<br> <br>(select id from syscolumns where name in ('SolutionId'))<br> <br>and type='U' and name not in ('SolutionComponentBase') and name not like '%ribbon%' -- ignore this table because it doesn't make a difference. it does cause dependency errors on the exported solution but we can manually edit the xml for that.<br> <br>order by name<br> <br><br> <br>select @count = count(\*) from @tables<br> <br>while (@count &gt; 0)<br> <br>begin<br> <br>select @currentTable =name, @currentM =ismanaged, @currentS =issolution from @tables where id=@count<br> <br><br> <br>if (@currentM = 1)<br> <br>begin<br> <br>select @sql ='update ' + @currentTable + ' set IsManaged=0 where SolutionId=N''' + cast(@solutionId as nvarchar(100)) + ''''<br> <br>exec (@sql)<br> <br><br> <br>print 'updated IsManaged to 0 on: ' + @currentTable<br> <br>end<br> <br><br> <br>if (@currentS = 1)<br> <br>begin<br> <br>select @sql ='update ' + @currentTable + ' set SolutionId=N''' + cast(@systemSolutionId as nvarchar(100)) + ''' where SolutionId=N''' + cast(@solutionId as nvarchar(100)) + ''''<br> <br>exec (@sql)<br> <br><br> <br>print 'updated SolutionId on: ' + @currentTable<br> <br>end<br> <br><br> <br>select @count = @count -1, @currentTable = NULL<br> <br>end<br>  |
| --- |



Thanks the author Gayan Perera who demos this in the video [https://channel9.msdn.com/Events/TechEd/NewZealand/TechEd-New-Zealand-2012/DYN401](https&#58;//channel9.msdn.com/Events/TechEd/NewZealand/TechEd-New-Zealand-2012/DYN401)
