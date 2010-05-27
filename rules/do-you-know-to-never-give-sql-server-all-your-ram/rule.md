---
type: rule
title: Do you know to never give SQL Server all your RAM?
uri: do-you-know-to-never-give-sql-server-all-your-ram
created: 2010-05-25T06:54:56.0000000Z
authors:
- id: 14
  title: Martin Hinshelwood

---

 This field should not be null (Remove me when you edit this field). 
1. Open SQL Server Management Studio
![](/Standards/ITAndNetworking/RulesToBetterSQLServerAdministration/PublishingImages/SQLServerManagementStudio_small.jpg)
2. Right click on the server name and select “Properties”
![](/Standards/ITAndNetworking/RulesToBetterSQLServerAdministration/PublishingImages/Properties_small.jpg)
3. Select the “Memory” tab 
![](/Standards/ITAndNetworking/RulesToBetterSQLServerAdministration/PublishingImages/MemoryTab_small.jpg)
4. You will see that the default number is HUGE. Change this to something more realistic. Let SQL use half of the memory in your server.Leave about 1024MB headroom. For example, if you server has 4GB of RAM, give the SQL server a Maximum server memory of 2048mb.
![](/Standards/ITAndNetworking/RulesToBetterSQLServerAdministration/PublishingImages/DefaultNumber_small.jpg)

 This will prevent SQL from “owning” all of the RAM on your system,leaving some memory left for your other applications to use.    
