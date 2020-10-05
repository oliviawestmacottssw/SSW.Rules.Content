---
type: rule
title: Do you know that Enum types should not be suffixed with the word "Enum"?
uri: do-you-know-that-enum-types-should-not-be-suffixed-with-the-word-enum
created: 2018-04-25T23:53:39.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

This is against the .NET Object Naming Conventions and inconsistent with the framework.
 
Public Enum ProjectLanguageEnum CSharp VisualBasic End Enum
 Bad - Enum type is suffixed with the word "Enum" 

Public Enum ProjectLanguage CSharp VisualBasic End Enum
Good - Enum type is not suffixed with the word "Enum" 

We have a program called [SSW Code Auditor](https&#58;//www.ssw.com.au/ssw/CodeAuditor/) to check for this rule.
 ​
