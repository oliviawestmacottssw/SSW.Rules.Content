---
type: rule
title: Do you avoid putting business logic into the presentation layer?
uri: do-you-avoid-putting-business-logic-into-the-presentation-layer
created: 2018-04-26T22:25:39.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

Be sure you are aware of what is business logic and what isn't. Typically, looping code will be placed in the business layer. This ensures that no redundant code is written and other projects can reference this logic as well.

 
private void btnOK\_Click(object sender, EventArgs e)
{
rtbParaText.Clear();
var query =
from p in dc.GetTable()
select p.ParaID;
foreach (var result in query)
{
var query2 =
from t in dc.GetTable()
where t.ParaID == result
select t.ParaText;
rtbParaText.AppendText(query2.First() + "\r\n");
}
}
 Bad Example: A UI method mixed with business logics


private void btnOK\_Click(object sender, EventArgs e)
{
string paraText = Business.GetParaText();
rtbParaText.Clear();
rtbParaText.Add(paraText);
}
Good Example : Putting business logics into the business project, just call the relevant method when needed
