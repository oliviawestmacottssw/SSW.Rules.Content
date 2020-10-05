---
type: rule
title: Do you use string interpolation when formatting strings
uri: do-you-use-string-interpolation-when-formatting-strings
created: 2020-01-29T05:13:02.0000000Z
authors:
- id: 66
  title: Liam Elliott
- id: 78
  title: Matt Wicks

---

String Interpolation - greatly reduces the amount of boilerplate code required when working with strings
Formatting strings on the fly was previously a task which required a stack of boilerplate code
 
​​var s = String.Format("Profit is ${0} this year", p.TotalEarnings - p.Totalcost);
​​​Figure: Bad Example - Using String.Format() makes the code difficult to read

​​​var s = "Profit is ${p.TotalEarnings - p.Totalcost} this year";
Figure: Good Example - String Interpolation is very human readable
