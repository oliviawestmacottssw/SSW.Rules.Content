---
type: rule
title: Do you know when anchor should "run at server"?
uri: do-you-know-when-anchor-should-run-at-server
created: 2016-08-24T22:33:39.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

**&lt;a&gt;** tag should **runat=“server"** \*ONLY\* if you need to change the target at runtime.

If you include **runat=“server"** for an HTML element that you do not need access to in code behind, you are introducing a whole lot of overhead you do not need.
 
We have a program called [SSW Code Auditor](https&#58;//www.ssw.com.au/ssw/CodeAuditor/) to check for this rule.
