---
type: rule
title: (Before starting) Do you follow a Test Driven Process?
uri: before-starting-do-you-follow-a-test-driven-process
created: 2011-11-18T03:52:57.0000000Z
authors:
- id: 5
  title: Justin King
- id: 6
  title: Tristan Kurniawan

---

 This field should not be null (Remove me when you edit this field). 
**Bad Process**1. Check out
2. Compile
3. Develop
4. Compile
5. Check In

A Bad Developer ![](/TFS/RulesToBetterVersionControlwithTFS(AKASourceControl)/PublishingImages/BeforeCoding.jpg) Figure: Before you start cooking prepare all your ingredients (aka before you start coding, "Get Latest" the right way)
**Good Process**1. Get latest
2. Compile
3. Run Unit Tests
4. If Tests pass then start developing
5. Check out
6. Develop
7. Compile
8. Run Unit Tests
9. Get Latest (Always do a Get Latest before checking in as code you didn't change could break your code)
10. Compile
11. Run Unit Tests
12. Check In if all tests passed
13. Wait for gated check-in (GC) to complete
14. Reconcile your workspace if it was successful
15. Check that Continuous Integration (CI) build was successful(If GC was skipped)

A Good DeveloperNote: You should have both a Gated-Check-in (GC) and a Continuous Integration (CI) build on every branch.   
