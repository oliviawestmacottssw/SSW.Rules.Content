---
type: rule
title: Do you use server side comments?
uri: do-you-use-server-side-comments
created: 2016-08-24T22:29:47.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

Use server side comments:

- Use **&lt;%-- Comment Here --%&gt;** instead of **&lt;!-- Comment Here --&gt;** (Does not get rendered to the client, saves us a few precious kilobytes)
- Use **CTRL + K, C** to comment and **CTRL + K, U** to uncomment
