---
type: rule
title: Do you look for Code Coverage?
uri: do-you-look-for-code-coverage
created: 2012-04-01T11:02:56.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 23
  title: Damian Brady
- id: 3
  title: Eric Phan
- id: 78
  title: Matt Wicks

---

 
Code Coverage shows how much of your code is covered by tests and can be a useful tool for showing how effective your unit testing strategy is.  However, it should be looked at with caution.
 
- ​You should focus on quality not quantity of tests.
- You should write tests for fragile code first and not waste time testing trivial methods
- Remember the 80-20 rule - a very high test coverage is a noble goal but there are diminishing returns.
- If you're modifying code, write the test first, then change the code, then run the test to make sure it passes.

![CodeCoverage_blurred.png](/SoftwareDevelopment/RulestobetterArchitectureandCodeReview/PublishingImages/CodeCoverage2010.png)
Figure: Code Coverage metrics in VS2010. This solution has a very high code coverage percentage (around 80% on average)

