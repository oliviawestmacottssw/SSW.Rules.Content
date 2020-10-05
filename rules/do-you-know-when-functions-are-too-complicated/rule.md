---
type: rule
title: Do you know when functions are too complicated?
uri: do-you-know-when-functions-are-too-complicated
created: 2020-03-12T21:53:03.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

​In general you should always be looking to simplify your code (e.g. heavily nested case statements). As a minimum look for the most complicated method you have and check that it needs simplifying.​​

In Visual Studio, there is inbuilt support for Cyclomatic Complexity analysis.​​​
 
​1. Go to Developer > Code Metrics > Generate for Solution

![ Cyclomatic Complexity analysis tool](CodeMetrics.gif)

2. Look at the largest Cyclomatic Complexity number and refactor.

![ Results from Cyclomatic analysis these metrics give an indication on how complicated functions are​Tip: Maintainability index > 85 is good and < 65 is hard to maintain](CyclomaticAnalysis.gif)
