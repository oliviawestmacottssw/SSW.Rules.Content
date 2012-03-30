---
type: rule
title: Do you use the repository pattern for data access?
uri: do-you-use-the-repository-pattern-for-data-access
created: 2012-03-30T05:16:01.0000000Z
authors:
- id: 23
  title: Damian Brady

---

 
The repository pattern is a great way to handle your data access layer and should be used wherever you have a need to retrieve data and turn it into business objects.
 
Even better, by providing a consistent repository base class, you can get all your CRUD operations while avoiding any plumbing code.

See [this blog post](http&#58;//brdy.in/xqrAFb) by Damian Brady for an example of how to implement a repository pattern for Entity Framework.

