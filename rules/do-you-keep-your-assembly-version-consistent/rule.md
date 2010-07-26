---
type: rule
title: Do you keep your Assembly Version Consistent?
uri: do-you-keep-your-assembly-version-consistent
created: 2009-04-28T07:03:16.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 17
  title: Ryan Tee

---

![](/Standards/SoftwareDevelopment/RulesToBetterDotNETProjects/PublishingImages/VersionConsistent1.jpg) 
Figure: Keep these two versions consistent If you are not using the GAC, it is important to keep AssemblyVersion, AssemblyFileVersion and AssemblyInformationalVersionAttribute the same, otherwise it can lead to support and maintenance nightmares. By default these version values are defined in the AssemblyInfo file. In the following examples, the first line is the version of the assembly and the second line is the actual version display in file properties.
[assembly: AssemblyVersion("2.0.\*")]
<br>[assembly: AssemblyFileVersion("1.0.0.3")] Bad example - the common assembly versioning method. [assembly: AssemblyVersion("2.0.\*")]
<br>[assembly: AssemblyFileVersion("2.0.\*")] 
<br>[assembly: AssemblyInformationalVersion("2.0.\*")] Good example - the best way for Assembly versioning (when not using the GAC) If you are using the GAC, you should adopt a single AssemblyVersion and AssemblyInformationalVersionAttribute and update the AssemblyFileVerison with each build.

[assembly: AssemblyVersion("2.0.0.0")]
<br>[assembly: AssemblyFileVersion("2.0.\*")]
<br>[assembly: AssemblyInformationalVersion("2.0.0.0")] Good example - the best way for Assembly versioning (when using the GAC) Note: It would be good if Microsoft changed the default behaviour of AssemblyInformationalVersionAttribute to default to the AssemblyVersion.[See Mikes suggestion for improving the version number in the comments here.](http&#58;//msdn.microsoft.com/en-us/library/system.reflection.assemblyinformationalversionattribute.aspx)
