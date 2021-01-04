---
type: rule
archivedreason: 
title: Do you know when functions are too complicated?
guid: 3198a586-9314-431d-8226-51dce77fac4f
uri: do-you-know-when-functions-are-too-complicated
created: 2020-03-12T21:53:03.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
related: []
redirects: []

---


<p class="ssw15-rteElement-P">​In general you should always be looking to simplify your code (e.g. heavily nested case statements). As a minimum look for the most complicated method you have and check that it needs simplifying.​​<br></p><p class="ssw15-rteElement-P">In Visual Studio, there is inbuilt support for Cyclomatic Complexity analysis.​​​<br></p>
<br><excerpt class='endintro'></excerpt><br>
<p>​1. Go to Developer > Code Metrics > Generate for Solution</p><dl class="image"><dt><img src="CodeMetrics.gif" alt="CodeMetrics.gif" /></dt><dd>Figure: Cyclomatic Complexity analysis tool</dd></dl><p>2. Look at the largest Cyclomatic Complexity number and refactor.</p><dl class="image"><dt><img src="CyclomaticAnalysis.gif" alt="CyclomaticAnalysis.gif" /></dt><dd>Figure: Results from Cyclomatic analysis these metrics give an indication on how complicated functions are</dd></dl>​Tip: Maintainability index > 85 is good and < 65 is hard to maintain<br>


