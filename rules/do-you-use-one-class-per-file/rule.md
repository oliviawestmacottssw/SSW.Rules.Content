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

 This field should not be null (Remove me when you edit this field). 
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
