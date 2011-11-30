---
type: rule
title: Do you know that branches are better than Labels?
uri: do-you-know-that-branches-are-better-than-labels
created: 2011-11-18T03:52:47.0000000Z
authors:
- id: 22
  title: David Klein
- id: 5
  title: Justin King
- id: 17
  title: Ryan Tee
- id: 6
  title: Tristan Kurniawan
- id: 23
  title: Damian Brady
- id: 24
  title: Adam Stephensen

---

 
Although labels are useful they can be changed after they have been created with no way to tell that they have been changed.
 ![](/TFS/RulesToBetterVersionControlwithTFS(AKASourceControl)/PublishingImages/TFSLabel.png)Figure: Bad example, labels can be edited after the fact (they are mutable)![](/Management/RulesToBetterBranchingAndBuilds/PublishingImages/tfslabe2.jpg)Figure: Good example, branches give absolute certainty of versions (they are immutable)
**Fact #1**: Creating a branch of 1GB of source code does not increase the size of your database by 1GB. It just adds a bunch of pointers. Only the differences are actually stored. 
**Fact #2**: When you delete a branch it is not really “deleted”, you are just ending the history. You can undelete at a later time.

**Tip**: Find deleted items by ticking “Tools | Options | Source Control | Visual Studio Team Foundation Server | Show deleted items in the Source Control Explorer”

