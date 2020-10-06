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
 <br>
![default logging levels](sp-diagnostic-logging.jpg)

![lots of "Medium" level search logsThis made us had 60GB logs for only 14 days.](sp-diagnostic-logging-2.jpg)
So the solution is to change to "diagnostic logging level" as below to reduce the log size:

![](sp-diagnostic-logging-3.jpg)
