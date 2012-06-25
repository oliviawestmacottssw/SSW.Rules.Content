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


<p>Visual Studio has architecture tools that let you analyse the solution structure. However,&#160;this feature is only available in Visual Studio Ultimate. If you want architecture tools for Visual Studio, but don't have Visual Studio Ultimate, then there are excellent third party solutions like nDepend.</p>
<p>nDepend is a great tool for analysing the dependencies between classes and assemblies in your projects.&#160; It can find issues and highlights them in red for easy discovery.</p>
<br><excerpt class='endintro'></excerpt><br>
<img class="ms-rteCustom-ImageArea" src="/SoftwareDevelopment/RulestobetterArchitectureandCodeReview/PublishingImages/ArchitectureToolsVS11.png" alt="architecturetools_vs11.png" /><span class="ssw-rteStyle-FigureNormal">Figure&#58; VS11 lets you generate a dependency graph for your solution.</span>
<img class="ms-rteCustom-ImageArea" src="/SoftwareDevelopment/RulestobetterArchitectureandCodeReview/PublishingImages/DependencyDiagramInVS11.png" alt="sqldeploy_dependencies.png" style="width&#58;600px;" />
<span class="ssw-rteStyle-FigureNormal">Figure&#58; The dependency graph in VS11 shows you some interesting information about how projects relate to each other</span>
<p>nDepend has a similar diagram that is a little messier, but the latest version also includes a &quot;Queries + Rules Explorer&quot; which is another code analysis tool</p>
<img class="ms-rteCustom-ImageArea" src="/SoftwareDevelopment/RulestobetterArchitectureandCodeReview/PublishingImages/nDependDependencyGraph.png" alt="nDepend.png" style="width&#58;600px;" />​
<span class="ssw-rteStyle-FigureNormal">Figure：nDepend Dependency Graph. Issues are highlighted in red for easy discovery.</span>
<p>Read more about nDepend&#58; <a href="http&#58;//www.ndepend.com/">http&#58;//www.ndepend.com/</a></p>
<p><strong>Warning&#58; </strong>nDepend doesn't yet support Visual Studio 2012 (Aka VS11) with a plugin.</p>


