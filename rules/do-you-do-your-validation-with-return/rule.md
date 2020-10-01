---
type: rule
title: Do you do your validation with Return?
uri: do-you-do-your-validation-with-return
created: 2018-04-25T23:05:48.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

The return statement can be very useful when used for validation filtering.
Instead of a deep nested If, use Return to provide a short execution path for conditions which are invalid.
 
private void AssignRightToLeft()
{
  // Validate Right 
  if (paraRight.SelectedIndex &gt;= 0)
  { 
    // Validate Left 
    if (paraLeft.SelectedIndex &gt;= 0)
    {
       string paraId = paraRight.SelectedValue.ToString();
       Paragraph para = new Paragraph();
       para.MoveRight(paraId);
       RefreshData();
    }
  }
}
Figure: Bad example - using nested if for validation



private void AssignRightToLeft()
{
  // Validate Right 
  if (paraRight.SelectedIndex &gt;= 0)
  {
    return; 
  }
  
  // Validate Left 
  if (paraLeft.SelectedIndex &gt;= 0)
  {
    return;
  }

  string paraId = paraRight.SelectedValue.ToString();
  Paragraph para = new Paragraph();
  para.MoveRight(paraId);
  RefreshData();
}
Figure: Good example - using Return to exit early if invalid
