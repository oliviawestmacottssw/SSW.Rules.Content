---
type: rule
title: Practices - Do you write small components?
uri: practices---do-you-write-small-components
created: 2016-04-22T22:43:46.0000000Z
authors:
- id: 55
  title: Steve Leigh

---

The Single Responsibility Principle is a well understood, and well-accepted tenant of good code design.  It states that a class should do one thing, and do it well – and an Angular component is no exception.

When designing components, keep them small, modular and reusable. For example, if you have a menu, put it into a menu component, don’t put it in your app component.
 ![ Bad example - Having just 3 components for the page makes it difficult to reuse, maintain and test](comp-1.png)
![ Good example - Splitting up the page into 11 components means they are small and targeted - and thus easy to maintain and test. Components can be reused on other pages](comp-2.png)
