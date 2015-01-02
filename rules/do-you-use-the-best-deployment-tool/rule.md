---
type: rule
title: Do you use the best deployment tool?
uri: do-you-use-the-best-deployment-tool
created: 2015-01-02T01:35:53.0000000Z
authors:
- id: 23
  title: Damian Brady
- id: 1
  title: Adam Cogan

---

 Often, deployment is either done manually, or as part of the build process. But deployment is a completely different step in your lifecycle. It's important that deployment be automated, but done separately from the build process. 
There are two main reasons you should separate your deployment from your build process:

1. You're not dependent on your servers for your build to succeed. Similarly, if you need to change deployment locations, or add or remove servers, you don't have to edit your build definition and risk breaking your build.
2. You want to make sure you're deploying the **\*same\*** (tested) build of your software to each environment. If your deployment step is part of your build step, you may be rebuilding each time you deploy to a new environment.


The best tool for deployments is [Octopus Deploy​](http&#58;//octopusdeploy.com/).




![SugarLearningOctopus.png](/PublishingImages/SugarLearningOctopus.png)

Figure: Good Example - SSW uses Octopus Deploy to deploy Sugar Learning



Octopus Deploy allows you to package your projects in Nuget packages, publish them to the Octopus server, and deploy the package to your configured environments. Advanced users can also perform other tasks as part of a deployment like running integration and smoke tests, or notifying third-party services of a successful deployment.




[Version 2.6 of Octopus Deploy](http&#58;//octopusdeploy.com/blog/2.6) introduced the ability to create a new release and trigger a deployment when a new package is pushed to the Octopus server. Combined with Octopack, this makes continuous integration very easy from Team Foundation Server.

