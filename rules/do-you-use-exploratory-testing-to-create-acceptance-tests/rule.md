---
type: rule
title: Do you use Exploratory Testing to create Acceptance Tests?
uri: do-you-use-exploratory-testing-to-create-acceptance-tests
created: 2013-08-07T22:15:34.0000000Z
authors:
- id: 23
  title: Damian Brady

---

In an agile team, pre-planning all your tests is not always the most efficient use of time for testers.  PBIs can change direction, scope, and priority, and pre-planned tests are likely to change.



Exploratory testing provides the best way to create repeatable tests from the acceptance criteria - as you need them.
 
There are two ways to run an exploratory test in Microsoft Test Manager.

[[badExample]]
| ![go to the Test tab, choose Do Exploratory Testing, choose a PBI, then click Explore. Too many steps](exploratory_2.png)

[[goodExample]]
| ![Right-click on a requirement in your test suite and choose "Explore requirement"](exploratory_1.png)

**Note: **You should always run an exploratory test against a PBI. This will automatically relate any bugs and test cases to that PBI (not to mention the exploratory test run).

When you start an Exploratory test, you don't see any test steps, but you can click on the title of the requirement to see its Acceptance Criteria.

![Clicking on the title will show you the Acceptance Criteria](show_criteria.png)
**Note:** [You should always have Acceptance Criteria on your PBIs!](/Pages/Do-Your-User-Stories-Include-Acceptance-Criteria.aspx)

If you find a bug while testing, click the **Create bug** button to add a bug related to the PBI.

![Creating a bug from exploratory test links to the PBI](create_bug.png)
By default, the reproduction steps will be populated with the last 10 actions you took (you can [change this and other defaults with configuration](http://geekswithblogs.net/TarunArora/archive/2011/12/14/mtm-11-configuration-settings-amp-customization.aspx)).  You can cut this down to just the relevant actions by clicking Change steps.

![You can change the repro steps captured in the bug very easily](change_bug_steps.png)
Now you have a bug, you should create a matching test case so you can verify when the bug is fixed.  This also gives you a handy regression test to help ensure the problem isn't reproduced later.

![Click Save and create test to create a matching test case](save_create_test.png)
Again, the steps are prepopulated from your bug steps.

![The test steps are prepopulated from the action recording](create_test.png)
### Related Links


- [Do you do exploratory testing?](/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&TermId=14be0d02-79ad-4286-8b78-4f28b0ed4eea)
