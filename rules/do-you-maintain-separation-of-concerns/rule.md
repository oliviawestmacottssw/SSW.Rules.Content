---
type: rule
title: Do you maintain separation of concerns?
uri: do-you-maintain-separation-of-concerns
created: 2018-04-23T21:35:57.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

One of the major issues people had back in the day with ASP (before ASP.NET) was the prevalence of "Spaghetti Code". This mixed  **Reponse.Write()** with actual code.
 
Ideally, you should keep design and code separate - otherwise, it will be difficult to maintain your application. Try to move all data access and business logic code into separate modules.

Bob Martin explains this best:


`youtube: https://www.youtube.com/embed/WpkDN78P884`
