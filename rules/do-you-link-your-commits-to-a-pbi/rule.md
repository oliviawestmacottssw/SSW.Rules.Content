---
type: rule
title: Do you link your commits to a PBI?
uri: do-you-link-your-commits-to-a-pbi
created: 2019-03-13T01:00:33.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 87
  title: Andreas Lengkeek
- id: 82
  title: Barry Sanders
- id: 58
  title: Jernej Kavka
- id: 84
  title: Patricia Barros

---

In order to get better clarity on what work is done, it's a good idea to connect your PBI's and tasks to the commits, branches and pull requests that relate to the item. All commits, branches and pull requests should be linked to a PBI.

![](no-linked-commit.png)Bad Example: No linked commit's, branches or pull requests

![](link-branch-to-pbi.png)Good Example: Git branch linked to PBI in TFS
 
Note: If you create your branches through Azure DevOps then you can link them during creation.

![](link-pbi-during-creation.png)Good Example: Using Azure DevOps to link PBI during creation
Here is a handy resource for linking work items:

https://devblogs.microsoft.com/devops/linking-work-items-to-git-branches-commits-and-pull-requests/

Note: You can setup Branch Policies on your main branches to enforce this behaviour.

![](add-branch-policy-for-linked-items.png)Good Example: Branch Policy on the master branch to enforce linked work items on pull requests
