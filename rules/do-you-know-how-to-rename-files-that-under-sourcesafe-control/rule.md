---
type: rule
title: Do you know how to rename files that under SourceSafe control?
uri: do-you-know-how-to-rename-files-that-under-sourcesafe-control
created: 2009-05-06T08:46:37.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 17
  title: Ryan Tee

---

Whenever we rename a file in Visual Studio .NET, the file becomes a new file in SourceSafe. If the file has been checked-out, the status of old file will remain as checked-out in SourceSafe.

The step by step to rename a file that under SourceSafe control:

1. Save and close the file in Visual Studio .NET, and check in the file if it is checked-out.
2. Open Visual SourceSafe Explorer and rename the file.
3. Rename it in Visual Studio .NET, click "Continue with change" to the 2 pop-up messages:
![ Warning message of renaming files under source control.![](RenameVSS2_small.jpg) ](RenameVSS1_small.jpg) 



 Visual Studio .NET should find the file under source control and it will come up with a lock icon
