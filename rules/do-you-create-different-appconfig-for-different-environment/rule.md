---
type: rule
title: Do You Create Different App.Config for Different Environment?
uri: do-you-create-different-appconfig-for-different-environment
created: 2009-12-10T05:23:58.0000000Z
authors:
- id: 11
  title: Andy Taslim

---

Every application has different settings depending on the environment it is running on, e.g. production, testing or development environment.
<br>It is much easier and efficient if app.config is provided in several environment types, so then the developer can just copy and paste the required app.config.

![ Bad Example - Only 1 App.config provided](AppConfigBad.jpg)
![](App.config.jpg)

Figure : Good Example - Several App.config are provided
