---
type: rule
archivedreason: 
title: Do you know when functions are too complicated?
guid: 3198a586-9314-431d-8226-51dce77fac4f
uri: do-you-know-when-functions-are-too-complicated
created: 2020-03-12T21:53:03.0000000Z
authors:
- id: 1
  title: Adam Cogan
related: []
redirects: []

---

In general you should always be looking to simplify your code (e.g. heavily nested case statements). As a minimum look for the most complicated method you have and check that it needs simplifying.

In Visual Studio, there is inbuilt support for Cyclomatic Complexity analysis.

<!--endintro-->

1. Go to Developer > Code Metrics > Generate for Solution

![Cyclomatic Complexity analysis tool](CodeMetrics.gif)
2. Look at the largest Cyclomatic Complexity number and refactor.

![Results from Cyclomatic analysis these metrics give an indication on how complicated functions areTip: Maintainability index > 85 is good and < 65 is hard to maintain](CyclomaticAnalysis.gif)
