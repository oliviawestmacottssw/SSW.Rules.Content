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

 This field should not be null (Remove me when you edit this field). 

```
[assembly: AssemblyVersion("2.0.*")]
[assembly: AssemblyFileVersionAttribute("1.0.0.3")]
```

Bad example - the common assembly versioning method. 

```
[assembly: AssemblyVersion("2.0.*")]
[assembly: AssemblyFileVersionAttribute("2.0.*")]
```

Good example - the best way for Assembly versioning. 
