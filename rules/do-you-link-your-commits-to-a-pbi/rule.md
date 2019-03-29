---
type: rule
archivedreason: 
title: Do you link your commits to a PBI?
guid: 0e206ce8-deed-4b09-902d-ecec0499586b
uri: do-you-link-your-commits-to-a-pbi
created: 2019-03-13T01:00:33.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
- title: Andreas Lengkeek
  url: https://ssw.com.au/people/andreas-lengkeek
- title: Barry Sanders
  url: https://ssw.com.au/people/barry-sanders
- title: Jernej Kavka
  url: https://ssw.com.au/people/jernej-kavka
- title: Patricia Barros
  url: https://ssw.com.au/people/patricia-barros
related: []
redirects: []

---


​​​​​​​In order to get better clarity on what work is done, it's a good idea to connect your PBI's and tasks to the commits, branches and pull requests&#160;that relate to the item.&#160;All commits, branches and pull requests should be linked to a&#160;PBI.​​<div><br></div><div><img src="/SiteAssets/do-you-link-your-commits-to-a-pbi/no-linked-commit.png" alt="no-linked-commit.png" style="margin&#58;5px;width&#58;518px;height&#58;167px;" />&#160;</div><div><dd class="ssw15-rteElement-FigureBad">​Bad Example&#58; No linked commit's, branches or pull requests<br></dd>​​<br><img src="/SiteAssets/do-you-link-your-commits-to-a-pbi/link-branch-to-pbi.png" alt="" style="margin&#58;5px;width&#58;518px;height&#58;182px;" /><dd class="ssw15-rteElement-FigureGood">Good Example&#58; Git branch linked to PBI in&#160;TFS<br></dd></div>
<br><excerpt class='endintro'></excerpt><br>
<p class="ssw15-rteElement-Tip">Note&#58; If you create your branches through Azure DevOps then you can link them during creation.​​​​​</p><p>​<img src="/SiteAssets/do-you-link-your-commits-to-a-pbi/link-pbi-during-creation.png" alt="link-pbi-during-creation.png" style="margin&#58;0px 5px;width&#58;518px;height&#58;401px;" /><br></p><dd class="ssw15-rteElement-FigureGood">​Good Example&#58; Using Azure DevOps to link PBI during creation<br></dd><p><br>Here is a handy resource for linking work items<br></p><p><a href="https&#58;//devblogs.microsoft.com/devops/linking-work-items-to-git-branches-commits-and-pull-requests/">https&#58;//devblogs.microsoft.com/devops/linking-work-items-to-git-branches-commits-and-pull-requests/​​​</a>​​</p><div><p class="ssw15-rteElement-Tip">Note&#58; You can setup&#160;Branch Policies on your main branches to enforce this behaviour.</p><p><img src="/SiteAssets/do-you-link-your-commits-to-a-pbi/add-branch-policy-for-linked-items.png" alt="add-branch-policy-for-linked-items.png" style="margin&#58;0px 5px;width&#58;523px;height&#58;308px;" /><br></p><dd class="ssw15-rteElement-FigureGood">​Good Example&#58; Branch Policy on the master branch to enforce linked work items on pull requests<br></dd></div>


