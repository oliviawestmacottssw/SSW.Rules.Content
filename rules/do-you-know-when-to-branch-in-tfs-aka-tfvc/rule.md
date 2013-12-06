---
type: rule
title: Do you know when to branch in TFS (aka TFVC)?
uri: do-you-know-when-to-branch-in-tfs-aka-tfvc
created: 2013-12-06T17:54:34.0000000Z
authors:
- id: 24
  title: Adam Stephensen

---

 
One of the most controversial issues we discuss is when to create branches.

Many smart people like creating braches e.g.     [http://blog.hinshelwood.com/archive/2010/04/14/guidance-a-branching-strategy-for-scrum-teams.aspx](http&#58;//blog.hinshelwood.com/archive/2010/04/14/guidance-a-branching-strategy-for-scrum-teams.aspx).

As outlined by Martin Fowler in his article on [Feature Branches](http&#58;//martinfowler.com/bliki/FeatureBranch.html) however, there are a number of issues related to merging that lead us to try and minimise the number of branches that we work with.
 
### Why we don’t like branching

1. Merging is painful, complex and is a time consuming task that does not add value.
2. Often regressions are introduced as merges are missed and not merged back to trunk
3. The longer branches are, the more people that have worked on them... the more unpleasant the merge is going to be.
 Amount of pain = size of the change \* the amount of work on the trunk in that period
4. The more you need to create a branch, the harder it is going to be to merge it back into the trunk!
5. Branching impedes refactoring.
 If a am working on a branch and perform sweeping renaming, and a developer working on another branch does the same – merging is nearly impossible.
 This is <br>      **very** likely to happen on code bases that require tidying when you have developers who believe in improving code as they go (see the <br>      [Boy Scout Rule](http&#58;//www.ssw.com.au/ssw/standards/Rules/RulestoBetterCode.aspx#BoyscoutRule))


### When we \*DO\* branch

- For a disposable, investigatory spike
- Every time we release​

<dl class="badImage"><dt>
      <img src="/TFS/RulesToBetterBranchingAndBuilds/PublishingImages/branch-bad.jpg" alt="">
   </dt><dd>Figure&#58; Bad Example – Creating a branch per feature leads to lots of merging (Image from<a href="http&#58;//paulhammant.com/blog/branch_by_abstraction.html"><span class="s2">http&#58;//paulhammant.com/blog/branch_by_abstraction.html</span></a>)</dd></dl><dl class="badImage"><dt>
      <img src="/TFS/RulesToBetterBranchingAndBuilds/PublishingImages/branch-bad-2.jpg" alt="">
   </dt><dd>Figure&#58; Bad Example – Creating a branch per sprint has everyone working on the same code but requires at least one merge every sprint</dd></dl><dl class="goodImage"><dt>
      <img src="/TFS/RulesToBetterBranchingAndBuilds/PublishingImages/branch-good.jpg" alt="">
   </dt><dd>Figure&#58; Good Example&#58; Release Branching - always develop on the trunk, but create a new branch each time you release.&#160;<br>This means th​at all developers are continually integrating all their code, branching is rare, but you always have access to your released version in case bug fixes or small mods are required.<br>(Image from&#160;<a href="http&#58;//paulhammant.com/blog/branch_by_abstraction.html"><span class="s2">http&#58;//paulhammant.com/blog/branch_by_abstraction.html</span></a>)</dd></dl>
Further reading:

- [http://continuousdelivery.com/2011/05/make-large-scale-changes-incrementally-with-branch-by-abstraction/](http&#58;//continuousdelivery.com/2011/05/make-large-scale-changes-incrementally-with-branch-by-abstraction/)
- [http://paulhammant.com/blog/branch\_by\_abstraction.html](http&#58;//paulhammant.com/blog/branch_by_abstraction.html)
- [http://martinfowler.com/bliki/FeatureBranch.html](http&#58;//martinfowler.com/bliki/FeatureBranch.html)
- [http://martinfowler.com/bliki/SemanticConflict.html](http&#58;//martinfowler.com/bliki/SemanticConflict.html)


