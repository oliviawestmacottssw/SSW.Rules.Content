---
type: rule
title: Do you know the best Unit Testing framework?
uri: do-you-know-the-best-unit-testing-framework
created: 2017-02-02T18:12:03.0000000Z
authors:
- id: 24
  title: Adam Stephensen

---

When getting started with unit testing, it is important to use the right tools for the job.
 ![bestunittest-bad1.png](bestunittest-bad1.png)![bestunittest-bad2.png](bestunittest-bad1.png)Bad Example: MS Test was the default testing library for previous versions of .NET and Visual Studio but lacked many features that were available in more complete tools like NUnit
![bestunittest-ok1.png](bestunittest-bad1.png)![bestunittest-ok2.png](bestunittest-bad1.png)OK Example: NUnit - For previous versions of .NET, NUnit was the best testing library but required work on the Continuous Integration server to get the unit tests to run in a CI environment. One of the key features that NUnit had that MS Test didn't was the TestCase attribute that allows you to specify inline data to be used when invoking that test
  ![bestunittest-good1.png](bestunittest-bad1.png)![bestunittest-good2.png](bestunittest-bad1.png)Good Example: XUnit comes out of the box with .NET Core and includes most of the great features of NUnit, while also being supported out of the box with Team Foundation Server and Visual Studio Team Services
