---
type: rule
title: Do you use the Lifecycles feature in Octopus Deploy?
uri: do-you-use-the-lifecycles-feature-in-octopus-deploy
created: 2015-01-02T02:10:20.0000000Z
authors:
- id: 23
  title: Damian Brady

---

 
[Octopus Deploy 2.6](http&#58;//octopusdeploy.com/blog/2.6) introduced a new Lifecycles feature that makes Continuous Integration from TFS much easier. It's a must have for projects in TFS that use Octopus for deployment.

As well as allowing continuous integration, the Lifecycles feature adds some good governance around when a project can be deployed to each environment.
 
Lifecycles can be found in the Library section of Octopus Deploy. By default, a project will use the Default Lifecycle which allows any deployment at any time.
<dl class="image"><dt><img src="/PublishingImages/Octopus_Lifecycles.png" alt="Octopus_Lifecycles.png"></dt><dd>Figure&#58; Lifecycles can be found in the Library</dd></dl>
You should create a new Lifecycle for each project you've configured with Octopus Deploy. You should set up a phase to continuously deploy to your first environment (e.g. test or staging), but make sure the final phase of the lifecycle is a manual step to production.
<dl class="image"><dt> <img src="/PublishingImages/SugarLearning_Lifecycle.png" alt="SugarLearning_Lifecycle.png"></dt><dd>Figure&#58; Good Example - This lifecycle has two phases&#58;&#160;an automatic release to a Staging server, and a manual release to the Production server.</dd></dl>
In the Process tab of your project definition, there's a panel on the right-hand side that lets you configure the Lifecycle to use. You should also enable Automatic Release Creation. If you have a CI build which publishes a new package to the Octopus NuGet feed as part of your build using OctoPack, and your first Lifecycle phase is automatic, this will result in continuous deployment to your CI environment.
<dl class="goodImage"><dt><img src="/PublishingImages/Lifecycle_CI.png" alt="Lifecycle_CI.png"></dt><dd>Figure&#58; Good Example -&#160;This combination results in Continuous Deployment to the Staging server when a new package is pushed</dd></dl> ​  
