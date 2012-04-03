---
type: rule
title: Do you look at the architecture?
uri: do-you-look-at-the-architecture
created: 2012-03-16T08:33:48.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 23
  title: Damian Brady
- id: 3
  title: Eric Phan

---

 
Visual Studio has architecture tools that let you analyse the solution structure. While these can be useful, they're not as good as nDepend at highlighting areas that should be looked at.

nDepend is a great tool for analysing the dependencies between classes and assemblies in your projects.  It can find issues and highlights them in red for easy discovery.
 
![architecturetools_vs11.png](/SoftwareDevelopment/RulestobetterArchitectureandCodeReview/PublishingImages/ArchitectureToolsVS11.png)
Figure: VS11 lets you generate a dependency graph for your solution.![sqldeploy_dependencies.png](/SoftwareDevelopment/RulestobetterArchitectureandCodeReview/PublishingImages/DependencyDiagramInVS11.png)
Figure: The dependency graph in VS11 shows you some interesting information, but it's not as good as nDepends at highlighting issues

nDepend is much better at showing you where your code architecture needs some work.

![nDepend.png](/SoftwareDevelopment/RulestobetterArchitectureandCodeReview/PublishingImages/nDependDependencyGraph.png)
Figure：nDepend Dependency Graph. Issues are highlighted in red for easy discovery.Read more about nDepend: [http://www.ndepend.com/](http&#58;//www.ndepend.com/)

Warning: nDepend doesn't yet support Visual Studio 2012 (AKA VS11) with a plugin.

