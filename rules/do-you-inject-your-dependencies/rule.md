---
type: rule
title: Do you inject your dependencies?
uri: do-you-inject-your-dependencies
created: 2012-10-19T17:23:08.0000000Z
authors:
- id: 24
  title: Adam Stephensen

---

Injecting your dependency gives you:

- Loosely coupled classes
- Increased code reusing
- Maintainable code
- Testable methods
- All dependencies are specified in one place
- Class dependencies are clearly visible in the constructor

 ![ Bad Example – A solution where each layer depends on static classes is not maintainable or testable ![inject ](inject-bad-1.jpg)
