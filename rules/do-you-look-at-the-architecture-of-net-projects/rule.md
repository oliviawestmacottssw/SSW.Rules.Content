---
type: rule
archivedreason: 
title: Do you look at the architecture of .NET projects?
guid: 94c385c2-98fd-46a0-acd1-b50070ee03ee
uri: do-you-look-at-the-architecture-of-net-projects
created: 2012-03-16T08:33:48.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
- title: Damian Brady
  url: https://ssw.com.au/people/damian-brady
- title: Eric Phan
  url: https://ssw.com.au/people/eric-phan
related:
- do-you-look-for-grasp-patterns
redirects: []

---


<p>Visual Studio has architecture tools that let you analyse the solution structure. While these can be useful, they're not as good as nDepend at highlighting areas that should be looked at.</p>
<p>nDepend is a great tool for analysing the dependencies between classes and assemblies in your projects.&#160; It can find issues and highlights them in red for easy discovery.</p>
<br><excerpt class='endintro'></excerpt><br>
<p><img alt="architecturetools_vs11.png" src="/SoftwareDevelopment/RulestobetterArchitectureandCodeReview/PublishingImages/ArchitectureToolsVS11.png" style="margin&#58;5px;" /><br><span class="ssw-rteStyle-FigureNormal">Figure&#58; VS11 lets you generate a dependency graph for your solution.</span><img alt="sqldeploy_dependencies.png" src="/SoftwareDevelopment/RulestobetterArchitectureandCodeReview/PublishingImages/DependencyDiagramInVS11.png" style="margin&#58;5px;width&#58;600px;height&#58;243px;" /><br><span class="ssw-rteStyle-FigureNormal">Figure&#58; The dependency graph in VS11 shows you some interesting information, but it's not as good as nDepend at highlighting issues</span></p>
<div><span>nDepend is much better at showing you where your code architecture needs some work.</span></div>
<img alt="nDepend.png" src="/SoftwareDevelopment/RulestobetterArchitectureandCodeReview/PublishingImages/nDependDependencyGraph.png" style="margin&#58;5px;width&#58;600px;height&#58;370px;" /><br><span class="ssw-rteStyle-FigureNormal">Figure：nDepend Dependency Graph. Issues are highlighted in red for easy discovery.</span> <p>Read more about nDepend&#58; <a href="http&#58;//www.ndepend.com/">http&#58;//www.ndepend.com/</a></p>
<div><span><strong>Warning&#58; </strong>nDepend doesn't yet support Visual Studio 2012 (Aka VS11) with a plugin.</span></div>


