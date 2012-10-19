---
type: rule
title: Do You Use a Dependency Injection Centric Architecture ?
uri: do-you-use-a-dependency-injection-centric-architecture-
created: 2012-10-19T19:11:41.0000000Z
authors:
- id: 24
  title: Adam Stephensen
- id: 40
  title: Igor Goldobin

---

 ![inject](/SoftwareDevelopment/RulesToBetterMVC/PublishingImages/dependency-inject-good.jpg)Figure: Bad Example – N-Tiered architectures do not inherently support dependency injection![inject](/SoftwareDevelopment/RulesToBetterMVC/PublishingImages/dependency-inject-good.jpg)Figure: Good Example – The Onion Architecture promotes layers built on interfaces, and then injecting dependencies into those layers. This keeps coupling low, and therefore maintainability high
The classes in each layer can depend on layers toward the centre.

It emphasizes the use of interfaces for the business logic and repository layers. The repository layer corresponds to the Data Access layer in an n-Tier architecture.

An n-Tier architecture has at its base the database.
 The core of the onion architecture is the Domain Model, and all dependencies are injected. This leads to more maintainable applications since it emphasizes separation of concerns.

