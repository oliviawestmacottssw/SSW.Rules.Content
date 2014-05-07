---
type: rule
title: Do you know the best Project/Version conventions?
uri: do-you-know-the-best-projectversion-conventions
created: 2011-11-18T03:52:36.0000000Z
authors:
- id: 22
  title: David Klein
- id: 5
  title: Justin King
- id: 17
  title: Ryan Tee
- id: 6
  title: Tristan Kurniawan

---

 
Having a good folder structure in version control allows everyone to know where everything is without even having to look.​
 

```
/northwind
 /trunk
 /branches (or shelvesets)
  /experiemental-feature1
 /releases (or tags)
  /1.0.0.356
```

Figure: Bad example, SVN conventions are a dated and ignore releases, hotfixes and Service Packs 
Trunk is the old way, Main is the new way as per the branching guidance, and it is the way that Microsoft does things.
![Main branch guidance ](/PublishingImages/BranchGuidance.jpg)Figure: Good example, this makes a lot more sense **More Information:** ![Good format for the information](/PublishingImages/GoodFormatForInfo.jpg)Figure: A good format for all your Products/Projects makes it easy to know where things are and what they are for 
Read the TFS 2010 Branching Guidance - [http://tfsbranchingguideiii.codeplex.com](http&#58;//tfsbranchingguideiii.codeplex.com/)

