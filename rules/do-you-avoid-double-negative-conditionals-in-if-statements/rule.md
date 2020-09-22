---
type: rule
title: Do you avoid Double-Negative Conditionals in if-statements?
uri: do-you-avoid-double-negative-conditionals-in-if-statements
created: 2018-04-24T22:03:21.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

 
Try to avoid Double-Negative Conditionals in if-statements. Double negative conditionals are difficult to read because developers have to evaluate what is positive state of two negatives. So always try to make a single positive when you write if-statement.
 
​if (!IsValid)
{
 // handle no error
}
else
{
 // handle error
}​


Figure: Bad e​xample​

if (IsValid)
{
 // handle error
}
else
{
 // handle no error
}


Figure: Good example​

if (!IsValid)
{
 // handle error
}
​Figure: Another good example​
