---
type: rule
title: Do you know how to format your MessageBox code?
uri: do-you-know-how-to-format-your-messagebox-code
created: 2018-04-25T23:10:49.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

You should always write each parameter of MessageBox in a separate line. So it will be more clear to read in the code. Format your message text in code as you want to see on the screen.
 
​Private Sub ShowMyMessage()
 MessageBox.Show("Are
 you sure you want to delete the team project """ + strProjectName
 + """?" + Environment.NewLine + Environment.NewLine + "Warning:
 Deleting a team project cannot be undone.", strProductName + "
 " + strVersion(), MessageBoxButtons.YesNo, MessageBoxIcon.Warning, MessageBoxDefaultButton.Button2)
Figure: Bad example of MessageBox code format​

Private Sub ShowMyMessage()
 MessageBox.Show( \_ 
 "Are you sure you want to delete the team project """ + strProjectName + """?"
 \_ + Environment.NewLine \_ +
 Environment.NewLine \_ +
 "Warning: Deleting a team project cannot be undone.", \_
 strProductName + " " + strVersion(), \_
 MessageBoxButtons.YesNo, \_
 MessageBoxIcon.Warning, \_
 MessageBoxDefaultButton.Button2)
End Sub


Figure: Good example of MessageBox code format​​
