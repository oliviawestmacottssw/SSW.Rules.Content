---
type: rule
title: Do you save failed experiments in abandoned pull requests?
uri: do-you-save-failed-experiments-in-abandoned-pull-requests
created: 2019-03-13T04:58:30.0000000Z
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

Assume you are creating a cool new feature. First you will create a new branch, create some commits, check it works, and submit a pull request. However, if you are not happy with the feature then don’t just delete the branch as normal. Instead, create a pull request anyway and set the status to Abandoned. Now, you can continue to delete your branch as normal.





This makes sure that we have a historical log of work completed, and still keeps a clean repository.




   
![Setup pull request for feature branch so that we have a history of the commits](create-pr-for-failed-branch.png)






![PR is abandoned with a deleted branch](abandoned-pr-for-branch.png)
