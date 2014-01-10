---
type: rule
title: Do you generate the VS Dependency Graph?
uri: do-you-generate-the-vs-dependency-graph
created: 2012-03-16T08:04:49.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 24
  title: Adam Stephensen
- id: 40
  title: Igor Goldobin

---

 
​Dependency graphs are important because they give you an indication of the coupling between the different components within your application.

A well architected application (ie. one that correctly follows the Onion Architecture) will be easy to maintain because it is loosely coupled.
  ​  ![](/SoftwareDevelopment/RulestobetterArchitectureandCodeReview/PublishingImages/TimePRODependence.png)Figure: Bad Example- The Visual Studio Dependency Graph is hard to read ​  ![TimePRODependence-good.png](/SoftwareDevelopment/RulestobetterArchitectureandCodeReview/PublishingImages/TimePRODependence-good.png)Figure: Good Example – The ReSharper Dependency graph groups dependencies based on Solution Folders. By having a <br>      [Consistent Solution Structure](/SoftwareDevelopment/RulesToBetterDotNETProjects/Pages/SolutionStructure.aspx) it is easy to see from your Dependency Graph if there is coupling between your UI and your Dependencies​  
