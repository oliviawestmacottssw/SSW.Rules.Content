---
type: rule
title: Do you know what will break and how to be ready for them?
uri: do-you-know-what-will-break-and-how-to-be-ready-for-them
created: 2009-11-02T21:18:21.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 3
  title: Eric Phan

---


Most of your reports (built in and custom) will be broken as the database schema has significantly changed.

To be ready for this, do a test migration and update any custom reports against the new database schema. That way, when your live server is up and running, your reports will be ready.

See [John Socha-Leialoha's post](http&#58;//www.socha.com/blogs/john/2009/10/upgrading-team-foundation-server-2008.html) for a good write up about what has changed and how to get your reports working.

