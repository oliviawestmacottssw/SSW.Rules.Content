---
type: rule
title: Do you use String.Empty instead of ""?
uri: do-you-use-stringempty-instead-of-
created: 2018-04-25T21:51:21.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

Considering the memory management of .NET Framework String.Empty will get higher performance then using "".
 
​public string myString     
{
 get
 {
 return ;
 }     
}
Figure: Bad code. Low performance​​

public string myString
{     
 get     
 {     
 return string.Empty;     
 }     
}​
   Figure: Good code. Higher performance

We have a program called [SSW Code Auditor](https&#58;//www.ssw.com.au/ssw/CodeAuditor/Rules.aspx#TimeSpan) to check for this rule.​
