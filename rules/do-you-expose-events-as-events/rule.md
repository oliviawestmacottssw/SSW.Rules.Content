---
type: rule
title: Do you expose events as events?
uri: do-you-expose-events-as-events
created: 2018-04-30T19:30:42.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

You should expose events as events.​
 
​ public Action
&lt; connectioninformation &gt; ConnectionProblem;
Bad code​

public event Action
&lt; connectioninformation &gt; ConnectionProblem;
​​​Good code​​
