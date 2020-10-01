---
type: rule
title: Do you use one class per file?
uri: do-you-use-one-class-per-file
created: 2009-05-05T02:03:55.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 17
  title: Ryan Tee

---

Each class definition should live in its own file.

Reasons:

Easy to locate class definitions outside the Visual Studio IDE (e.g. SourceSafe, Windows Explorer)

The only exception should be - classes that collectively forms one atomic unit of reuse should live in one file. For example:


```
class MyClass
 
{

        ...

}


class MyClassAEventArgs

{

        ...

}


class MyClassBEventArgs

{

        ...

}


class MyClassAException

{

        ...

}


class MyClassBException

{

        ...

}
```

Bad example - 1 project, 1 file.
