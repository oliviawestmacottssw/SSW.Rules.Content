---
type: rule
title: Do you describe types sparsely?
uri: do-you-describe-types-sparsely
created: 2016-04-28T19:44:54.0000000Z
authors:
- id: 55
  title: Steve Leigh

---

This comes down to personal preference, but there are only a few times when you must define a type in TypeScript, for example:

1. When initializing a variable with an ambiguous value (eg. null)
2. Function parameters


Of course, there are also times when you may want to be more explicit – you may want to have an interface as a function return value instead of the class, for example.
 
The rest of the time, rely on TypeScript to infer the type for you.
![ Except for the input parameter, TypeScript can infer all the types for this function](describe.png)
