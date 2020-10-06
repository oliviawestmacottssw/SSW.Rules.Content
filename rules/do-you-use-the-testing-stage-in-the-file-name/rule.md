---
type: rule
title: Do you use the testing stage, in the file name?
uri: do-you-use-the-testing-stage-in-the-file-name
created: 2018-04-23T21:52:42.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

When moving through the different stages of testing i.e. from internal testing, through to UAT, you should suffix the application name with the appropriate stage:
 

| **Stage**  | **Testing Description**  | **Naming Convention**  |
| --- | --- | --- |
| Alpha | Developer testing with project team | Northwind\_v2-3\_alpha.exe |
| Beta | Internal “Test Please" testing with non-project working colleagues | Northwind\_v2-3\_beta.exe |
| Production e.g. | When moving onto production, this naming convention is dropped | Northwind\_v2-3.exe |
