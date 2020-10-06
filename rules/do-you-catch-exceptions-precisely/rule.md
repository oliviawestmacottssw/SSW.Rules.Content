---
type: rule
title: Do you catch exceptions precisely?
uri: do-you-catch-exceptions-precisely
created: 2013-09-11T19:22:41.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 38
  title: Drew Robson

---

In the try and catch block, if you always catch for normal     [Exception](http&#58;//msdn.microsoft.com/en-us/library/system.exception.aspx) you will never know where the true problem is. When using try you should always expect some exception may happen, so in our code we always catch the specific exceptions.
 

```
try 
{ 
     connection.Open();
}
catch (Exception ex) 
{ 
     return ex.ToString ();
}
```

Bad code – Catching the general Exception

```
try 
{ 
     connection.Open(); 
}
catch (InvalidOperationException ex) 
{ 
     return ex.ToString(); 
}
catch (SqlException ex) 
{ 
     return ex.ToString(); 
}
```

Good code - Catch with specific Exception
We have a program called  [SSW Code Auditor to check for this rule.](http&#58;//www.ssw.com.au/ssw/CodeAuditor/Rules.aspx#Except)
