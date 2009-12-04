---
type: rule
title: Do you name your assemblies consistently (<CompanyName>.<ComponentName>)?
uri: do-you-name-your-assemblies-consistently-companynamecomponentname
created: 2009-04-28T02:16:10.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 17
  title: Ryan Tee

---

 This field should not be null (Remove me when you edit this field). 

```
System.IO
```


contains all the classes that deal with inputs and outputs. As a general rule of thumb your assemblies should be named as follows:

&lt;CompanyName&gt;.&lt;ComponentName&gt; (e.g. SSW.Framework)

This allows a developer to know who developed the assembly and give the developer a general idea of what the assembly can be used for.

