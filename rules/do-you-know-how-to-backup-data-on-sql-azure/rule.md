---
type: rule
title: Do You Know How to Backup Data on SQL Azure?
uri: do-you-know-how-to-backup-data-on-sql-azure
created: 2015-01-29T02:15:44.0000000Z
authors:
- id: 44
  title: Duncan Hunter

---

 
Microsoft Azure SQL Database has built-in backups to support self-service Point in Time Restore and Geo-Restore for Basic, Standard, and Premium service tiers.
 
​Built-in Automatic Backup in Azure SQL Databas

Azure SQL Database automatically creates backups of every active database using the following schedule: Full database backup once a week, differential database backups once a day, and transaction log backups every 5 minutes. The full and differential backups are replicated across regions to ensure availability of the backups in the event of a disaster.

**Backup Storage**

Backup storage is the storage associated with your automated database backups that are used for Point in Time Restore and Geo-Restore. Azure SQL Database provides up to 200% of your maximum provisioned database storage of backup storage at no additional cost.


| Service Tier | Geo-Restore | Self-Service Point in Time Restore | Backup Retention Period | Restore a Deleted Database |
| --- | --- | --- | --- | --- |
| Web | Not supported | Not supported | n/a | n/a |
| Business | Not supported | Not supported | n/a | n/a |
| Basic | Supported | Supported | 7 days | √ |
| Standard | Supported | Supported | 14 days | √ |
| Premium | Supported | Supported | 35 days | √​ |


Learn more:

- ​Microsoft Documentation: Azure SQL Database Backup and Restore​






