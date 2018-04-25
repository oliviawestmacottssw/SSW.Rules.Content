---
type: rule
archivedreason: 
title: Do you do your validation with Return?
guid: bcd97bcb-132f-493e-87e7-67d5799d9c72
uri: do-you-do-your-validation-with-return
created: 2018-04-25T23:05:48.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
related: []
redirects: []

---


<p class="ssw15-rteElement-P">The Exit Sub statement can be very useful when used for validation filtering.<br>Instead of a deep nested If, use Exit Sub or Return to provide a short execution path for conditions which are invalid.<br></p>
<br><excerpt class='endintro'></excerpt><br>
<p class="ssw15-rteElement-CodeArea">Private Sub AssignRightToLeft() <br>'Validate Right <br>If lstParaRight.SelectedIndex &gt;= 0 Then <br>'Validate Left <br>If lstParaLeft.SelectedIndex &gt;= 0 Then <br>Dim paraID As String = lstParaRight.SelectedValue.ToString <br>Dim mParagraph As BusinessLayer.Paragraph = New Paragraph <br>mParagraph.MoveRight(paraID) <br>RefreshData() <br>End If <br>End If<br>End Sub&#160;</p><dd class="ssw15-rteElement-FigureBad">Figure&#58; Bad example -&#160;using nested if for validation<br></dd><p>​<br></p><p class="ssw15-rteElement-CodeArea">Private Sub AssignRightToLeft() <br>'Validate Right and Left <br>If lstParaRight.SelectedIndex = -1 Then Return<br>If lstParaLeft.SelectedIndex = -1 Then Return <br>Dim paraID As String = lstParaRight.SelectedValue.ToString <br>Dim mParagraph As BusinessLayer.Paragraph = New Paragraph <br>mParagraph.MoveRight(paraID) <br>RefreshData() <br>End If<br>End If<br>End Sub</p><dd class="ssw15-rteElement-FigureGood">Figure&#58; Good example -&#160;using Exit Sub to exit early if invalid ​<br></dd>


