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

 
To visualize the structure of all your code you need architecture tools that will analyse your whole solution.

They show the dependencies between classes and assemblies in your projects.
 You have 2 choices:

- Visual Studio's Dependency Graph. This feature is only available in Visual Studio Ultimate. (recommended)
- If you want architecture tools for Visual Studio, but don't have Visual Studio Ultimate, then the excellent 3rd party solution nDepend. A bonus is that it can also find issues and highlights them in red for easy discovery.

![architecturetools_vs11.png](/SoftwareDevelopment/RulestobetterArchitectureandCodeReview/PublishingImages/ArchitectureToolsVS11.png)Figure: VS11 lets you generate a dependency graph for your solution.![sqldeploy_dependencies.png](/SoftwareDevelopment/RulestobetterArchitectureandCodeReview/PublishingImages/DependencyDiagramInVS11.png)Figure: The dependency graph in VS11 shows you some interesting information about how projects relate to each other
nDepend has a similar diagram that is a little messier, but the latest version also includes a "Queries + Rules Explorer" which is another code analysis tool
![nDepend.png](/SoftwareDevelopment/RulestobetterArchitectureandCodeReview/PublishingImages/nDependDependencyGraph.png)​ Figure：nDepend Dependency Graph. Issues are highlighted in red for easy discovery.
Read more about nDepend: [http://www.ndepend.com/](http&#58;//www.ndepend.com/)

**Warning: **nDepend doesn't yet support Visual Studio 2012 (Aka VS11) with a plugin.

