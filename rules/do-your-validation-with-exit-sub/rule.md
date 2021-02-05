---
type: rule
archivedreason: 
title: Do you do your validation with Return?
guid: bcd97bcb-132f-493e-87e7-67d5799d9c72
uri: do-your-validation-with-exit-sub
created: 2018-04-25T23:05:48.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
related: []
redirects:
- do-you-do-your-validation-with-return

---


<p class="ssw15-rteElement-P">The return&#160;statement can be very useful when used for validation filtering.<br>Instead of a deep nested If, use Return to provide a short execution path for conditions which are invalid.<br></p>
<br><excerpt class='endintro'></excerpt><br>
<p class="ssw15-rteElement-CodeArea">private void AssignRightToLeft()<br>&#123;<br>&#160; // Validate Right&#160;<br>&#160; if (paraRight.SelectedIndex &gt;= 0)<br>&#160; &#123;&#160;<br>&#160; &#160; // Validate Left&#160;<br>&#160; &#160; if (paraLeft.SelectedIndex &gt;= 0)<br>&#160; &#160; &#123;<br>&#160; &#160; &#160; &#160;string paraId = paraRight.SelectedValue.ToString();<br>&#160; &#160; &#160; &#160;Paragraph para = new Paragraph();<br>&#160; &#160; &#160; &#160;para.MoveRight(paraId);<br>&#160; &#160; &#160; &#160;RefreshData();<br>&#160; &#160; &#125;<br>&#160; &#125;<br>&#125;​</p><dd class="ssw15-rteElement-FigureBad">Figure&#58; Bad example -&#160;using nested if for validation<br></dd><p>​<br></p><p class="ssw15-rteElement-CodeArea">private void AssignRightToLeft()<br>&#123;<br>&#160; // Validate Right&#160;<br>&#160; if (paraRight.SelectedIndex &gt;= 0)<br>&#160; &#123;<br>&#160; &#160; return;&#160;<br>&#160; &#125;<br>&#160;&#160;<br>&#160; // Validate Left&#160;<br>&#160; if (paraLeft.SelectedIndex &gt;= 0)<br>&#160; &#123;<br>&#160; &#160; return;<br>&#160; &#125;<br><br>&#160; string paraId = paraRight.SelectedValue.ToString();<br>&#160; Paragraph para = new Paragraph();<br>&#160; para.MoveRight(paraId);<br>&#160; RefreshData();<br>&#125;<br></p><dd class="ssw15-rteElement-FigureGood">Figure&#58; Good example -&#160;using Return&#160;to exit early if invalid ​<br></dd>


