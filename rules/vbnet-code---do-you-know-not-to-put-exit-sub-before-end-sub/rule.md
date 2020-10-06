---
type: rule
title: VB.NET Code - Do you know not to put Exit Sub before End Sub?
uri: vbnet-code---do-you-know-not-to-put-exit-sub-before-end-sub
created: 2018-04-30T22:32:50.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

This is often a bad practice if you already are ending Sub you don't need another line.
 
Sub MySub
…
End Sub
Exit sub


Figure: Bad example
Sub MySub
…
End sub


Figure: Good example
