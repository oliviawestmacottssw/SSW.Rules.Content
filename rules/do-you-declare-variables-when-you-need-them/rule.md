---
type: rule
archivedreason: Rule is outdated. Prefer shorter methods that eliminate the need for this rule
title: Do you declare variables when you need them?
guid: 24d23856-bd1a-42c5-b883-793e6c84366a
uri: do-you-declare-variables-when-you-need-them
created: 2018-04-24T21:55:53.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
related: []
redirects: []

---


<p class="ssw15-rteElement-P">Should you declare variables at the top of the function, or declare them when you need to use them? If you come back to your code after a few weeks and you no longer need a variable, you are quite likely to forget to delete the declaration at the top, leaving orphaned variables. Here at SSW, we believe that variables should be declared as they are needed.​<br></p>
<br><excerpt class='endintro'></excerpt><br>
<p class="ssw15-rteElement-CodeArea">​Private Sub Command0_Click()<br>Dim dteTodayDate As Date<br>Dim intRoutesPerDay As Integer<br>Dim intRoutesToday As Integer<br>Dim dblWorkLoadToday As Double<br>dblWorkLoadToday = Date.Now()<br>.<br>....many lines of code...<br>.<br>intRoutesPerDay = 2<br>End Sub</p><dd class="ssw15-rteElement-FigureBad">  Figure&#58; Bad example <br></dd><p><br></p><p class="ssw15-rteElement-CodeArea">Private Sub Command0_Click()<br>Dim dteTodayDate As Date<br>dteTodayDate = Date.Now()<br>.<br>....many lines of code...<br>.<br>Dim intRoutesPerDay As Integer<br>intRoutesPerDay = 2<br>.<br>....continuing code...<br>.End Sub</p><dd class="ssw15-rteElement-FigureGood">​Figure&#58; Good example​​<br></dd>


