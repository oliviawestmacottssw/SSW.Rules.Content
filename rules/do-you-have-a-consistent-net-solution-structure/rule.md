---
type: rule
title: Do you have a consistent .NET Solution Structure?
uri: do-you-have-a-consistent-net-solution-structure
created: 2009-04-24T03:31:54.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 24
  title: Adam Stephensen

---

 
When developing software, we follow a standard solution structure.
 ![solutionlayout.png](/SoftwareDevelopment/RulesToBetterDotNETProjects/PublishingImages/solution-structure.png)Figure: Good Example - The Solution and Projects are named consistently and follow the Onion Architecture ​​Dependencies and the application core are clearly separated as per the <br>   [Onion Architecture](/SoftwareDevelopment/RulesToBetterMVC/Pages/Use-a-Dependency-Injection-Centric-Architecture.aspx).
In the above example you can clearly see:

- The different layers of the Onion Architecture: see <br>      [Layers of the Onion Architecture](/SoftwareDevelopment/RulesToBetterMVC/Pages/The-layers-of-the-onion-architecture.aspx)
- Unit test and integration test projects: see[Rules to Better Unit Tests](http&#58;//www.ssw.com.au/ssw/standards/rules/RulesToBetterUnitTests.aspx)
- The Documentation solution folder: see <br>      [Do you review the documentation?](/SoftwareDevelopment/RulestobetterArchitectureandCodeReview/Pages/DoYouReviewTheDocumentation.aspx)​
- The References solution folder: to hold any 3rd party assemblies that are not available via NuGet


Common Library projects are named     **[Company].[AssemblyName]**. E.g.     **BCE.Logging** is a shared project between all solutions at company BCE.

Other projects are named     **[Company].[Solution Name].[AssemblyName]**. E.g.     **BCE.Sparrow.Business** is the Business layer assembly for company ‘BCE’, solution ‘Sparrow’.

We have separated the unit tests, one for each project, for several reasons:

- It provides a clear separation of concerns and allows each component to be individually tested
- The different libraries can be used on other projects with confidence as there are a set of tests around them


