---
type: rule
title: Do you catch and re-throw exceptions properly?
uri: do-you-catch-and-re-throw-exceptions-properly
created: 2013-09-11T21:16:44.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 38
  title: Drew Robson

---

A good catch and re-throw will make life easier while debugging, a bad catch and re-throw will ruin the exception's stack trace and make debugging difficult.
 

```
catch {} 
(Never use an empty catch block. Do something in the block or remove it.)

catch (SomeException) {} 
(Never use an empty catch block. Do something in the block or remove it.)

catch { throw; } 
(Never use an empty catch block. Do something in the block or remove it.)
catch (SomeException) { throw; } 
(Never use an empty catch block. Do something in the block or remove it.)
catch (SomeException ex) { throw ex; } 
(Never re-throw exceptions by passing the original exception object. Wrap the exception or use throw; instead.)

catch (SomeException ex) { someMethod(); throw ex; } 
(Never re-throw exceptions by passing the original exception object. Wrap the exception or use throw; instead.)
```

Bad Example - Bad code

```
catch (SomeException ex) 
{ 
     someMethod(); 
     throw; 
}

catch (SomeException ex) 
{ 
     someMethod(); 
     SomeOtherException wrapperEx = new SomeOtherException("This is a wrapper exception", ex);
     throw wrapperEx; 
}
```

Good Example - Good code
We have a program called [SSW Code Auditor](http&#58;//www.ssw.com.au/ssw/CodeAuditor/Default.aspx) to check for this rule.
