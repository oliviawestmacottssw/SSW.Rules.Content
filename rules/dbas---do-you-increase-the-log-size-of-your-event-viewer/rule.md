---
type: rule
title: DBAs - Do you increase the Log Size of your Event Viewer?
uri: dbas---do-you-increase-the-log-size-of-your-event-viewer
created: 2019-11-22T20:19:16.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

Change the defaults from 20480KB to 64000KB and Overwrite as needed. This will allow the users to view Security audits and errors much further into the past with a minimal increase in space - and it will never bloat your server.
 
[[badExample]]
| ![Using a small log size](EventViewer_BadSmallLogSize.png)

[[goodExample]]
| ![Using a reasonable log size](EventViewer_GoodReasonableLogSize.png)
