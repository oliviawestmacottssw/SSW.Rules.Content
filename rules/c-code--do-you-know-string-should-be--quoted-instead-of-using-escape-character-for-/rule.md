---
type: rule
title: C# Code- Do you know String should be @-quoted instead of using escape character for "\\"?
uri: c-code--do-you-know-string-should-be--quoted-instead-of-using-escape-character-for-
created: 2018-04-30T22:20:15.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

 
The @ symbol specifies that escape characters and line breaks should be ignored when the string is created.

As per:  [Strings](http&#58;//msdn.microsoft.com/en-us/library/c84eby0h%28v=vs.90%29.aspx)
 
​string p2 = "\\My Documents\\My Files\\";
Figure: Bad example - Using "\\"
string p2 = @"\My Documents\My Files\";
Figure: Good example - Using @​​

