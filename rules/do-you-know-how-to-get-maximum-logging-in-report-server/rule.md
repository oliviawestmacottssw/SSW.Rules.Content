---
type: rule
title: Do you know how to get maximum logging in Report Server?
uri: do-you-know-how-to-get-maximum-logging-in-report-server
created: 2016-09-12T00:39:48.0000000Z
authors:
- id: 3
  title: Eric Phan

---

By default SSRS will track reporting execution for the last 60 days. This might be OK in most cases, but you may want to adjust the retention days if you want better report usage statistics.
 
​T​o update the value you can:

1. ​​​Connect to the ReportServer database in SQL Management Studio
2. Execute the following script and update the value to the number of days you want to track




​​EXEC SetConfigurationInfo @Name=N'ExecutionLogDaysKept',@Value=N'365'



After you have this, you can query the ExecutionLog table to find useful information about report execution like:

- ​Which users are actively using the reports
- How long reports are executing
- The last time a report was executed
