---
type: rule
title: Do you avoid publishing from Visual Studio?
uri: do-you-avoid-publishing-from-visual-studio
created: 2013-02-06T18:47:32.0000000Z
authors:
- id: 24
  title: Adam Stephensen

---

 
Publishing from Visual Studio is a convenient way to deploy a web application, but it relies on a single developer’s machine which can lead to problems. Deploying to production should be easily repeatable, and able to be performed from different machines.
 
A better way to deploy is by using a defined Build in TFS.
![](/PublishingImages/test-publish.jpg)Figure: Bad Example – Using Publish to deploy ![](/PublishingImages/queuing-new-build.jpg)Figure: Good Example – Queuing a new build to deploy your application![](/PublishingImages/continuous-integration.jpg)Figure: Best example – Use continuous integration to trigger your Continuous Deployment build
