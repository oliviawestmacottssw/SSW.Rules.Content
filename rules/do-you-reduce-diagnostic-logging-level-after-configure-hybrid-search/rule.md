---
type: rule
title: Do you reduce diagnostic logging level after configure hybrid search?
uri: do-you-reduce-diagnostic-logging-level-after-configure-hybrid-search
created: 2017-04-25T23:51:08.0000000Z
authors:
- id: 9
  title: William Yin

---

 By default, SharePoint diagnostic logging level was set to “Information” and “Medium”, which will log quite a big info, and it increased a log after configuring “hybrid search”:
 ​​​<br>![sp-diagnostic-logging.jpg](sp-diagnostic-logging.jpg)Figure: default logging levels​
![sp-diagnostic-logging-2.jpg](sp-diagnostic-logging-2.jpg)Figure: lots of "Medium" level search logsThis made us had 60GB logs for only 14 days.
So the solution is to change to "diagnostic logging level" as below to reduce the log size:​
![sp-diagnostic-logging-3.jpg](sp-diagnostic-logging-3.jpg)
