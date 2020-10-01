---
type: rule
title: Do you know how to avoid problems in if-statements?
uri: do-you-know-how-to-avoid-problems-in-if-statements
created: 2018-04-24T22:00:00.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

Try to avoid problems in if-statements without curly brackets and just one statement which is written one line below the if-statement. Use just one line for such if-statements. If you want to add more statements later on and you could forget to add the curly brackets which may cause problems later on.
 
if (ProductName == null) ProductName = string.Empty; if (ProductVersion == null)
 ProductVersion = string.Empty; if (StackTrace == null) StackTrace = string.Empty;
Figure: Bad Example

if (ProductName == null) 
{ 
 ProductName = string.Empty; 
} 
if (ProductVersion == null)
{ 
 ProductVersion = string.Empty; 
} 
if (StackTrace == null) 
{ 
 StackTrace = string.Empty;
}
Figure: Good Example
