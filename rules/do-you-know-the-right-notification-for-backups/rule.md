---
type: rule
title: Do you know the right notification for backups?
uri: do-you-know-the-right-notification-for-backups
created: 2017-07-10T23:20:11.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

You need to log a record on success so you can check for backups that have failed. 
 ![ Bad example - an email is sent on completion![backup_notification_good.jpg](backup_notification_good.jpg)](backup_notification_bad.jpg)
Now you are able to be aware of missing backups. You can make automatically notification based on above table e.g. [by SQL Reporting Services data-driven subscription](https://www.ssw.com.au/ssw/KB/KB.aspx?KBID=Q1455840)
