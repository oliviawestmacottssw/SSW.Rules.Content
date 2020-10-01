---
type: rule
title: Do you know Windows Forms should have a minimum size to avoid unexpected UI behavior
uri: do-you-know-windows-forms-should-have-a-minimum-size-to-avoid-unexpected-ui-behavior
created: 2015-06-30T08:31:56.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

If windows form does not setup a minimum size, your users could have unpredictable form behaviour as seen below:
![ Bad Example - Unexpected window form](../../assets/Bugsize.gif)

 
Therefore, a standard has been built to ensure Windows forms have a minimum size.
![ Good Example - User friendly window form](../../assets/Minisize.gif)
