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

 This field should not be null (Remove me when you edit this field). 
1. Save and close the file in Visual Studio .NET, and check in the file if it is checked-out.
2. Open Visual SourceSafe Explorer and rename the file.
3. Rename it in Visual Studio .NET, click "Continue with change" to the 2 pop-up messages:
![](/Standards/SoftwareDevelopment/RulesToBetterDotNETProjects/PublishingImages/RenameVSS1_small.jpg) Figure: Warning message of renaming files under source control.![](/Standards/SoftwareDevelopment/RulesToBetterDotNETProjects/PublishingImages/RenameVSS2_small.jpg) Figure: You are seeing this as the new file name already exists in SourceSafe, just click "Continue with change".



Visual Studio .NET should find the file under source control and it will come up with a lock icon  
