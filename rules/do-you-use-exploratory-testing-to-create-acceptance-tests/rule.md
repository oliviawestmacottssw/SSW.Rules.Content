---
type: rule
title: Do you use Exploratory Testing to create Acceptance Tests?
uri: do-you-use-exploratory-testing-to-create-acceptance-tests
created: 2013-08-07T22:15:34.0000000Z
authors:
- id: 23
  title: Damian Brady

---

 In an agile team, pre-planning all your tests is not always the most efficient use of time for testers.  PBIs can change direction, scope, and priority, and pre-planned tests are likely to change.



Exploratory testing gives you an easy way to create repeatable tests from the acceptance criteria - as you need them.
   There are two ways to run an exploratory test in Microsoft Test Manager.



![exploratory_2.png](/SoftwareDevelopment/RulesToBetterUserAcceptanceTests/PublishingImages/exploratory_2.png)

Figure: Bad Example - go to the Test tab, choose Do Exploratory Testing, choose a PBI, then click Explore. Too many steps.



![exploratory_1.png](/SoftwareDevelopment/RulesToBetterUserAcceptanceTests/PublishingImages/exploratory_1.png)

Figure: Good Example - Right-click on a requirement in your test suite and choose Explore requirement
**Note: **You should always run an exploratory test against a PBI. This will automatically relate any bugs and test cases to that PBI (not to mention the exploratory test run).




When you run an Exploratory test, you don't see any test steps, but you can click on the title of the requirement to see its Acceptance Criteria.




![show_criteria.png](/SoftwareDevelopment/RulesToBetterUserAcceptanceTests/PublishingImages/show_criteria.png)


**Figure: Clicking on the title will show you the Acceptance Criteria**

