---
type: rule
title: Do you always make file paths @-quoted?
uri: do-you-always-make-file-paths--quoted
created: 2009-05-13T06:57:56.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 17
  title: Ryan Tee

---

 This field should not be null (Remove me when you edit this field). 
By inserting an @ character in front of the string, e.g. **@"C:\Temp\MyFile.txt"**, you can turn off escape sequences, making it behave like VB.NET. File paths should always be stored like this in strings.


| We have a program called [SSW Code Auditor](http&#58;//www.ssw.com.au/ssw/CodeAuditor/) to check for this rule. |
| --- |


