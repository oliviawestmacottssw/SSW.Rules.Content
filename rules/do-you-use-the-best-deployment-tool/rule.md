---
type: rule
archivedreason: 
title: Do you use the best deployment tool?
guid: 7af442fc-db9a-43d2-afdd-7dfcbeb50f89
uri: do-you-use-the-best-deployment-tool
created: 2015-01-02T01:35:53.0000000Z
authors:
- title: Damian Brady
  url: https://ssw.com.au/people/damian-brady
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
related:
- do-you-know-when-to-use-an-on-premises-build-server-with-visual-studio-online
- do-you-estimate-all-tasks-at-the-start-of-the-sprint
- do-you-use-the-lifecycles-feature-in-octopus-deploy
redirects: []

---


Often, deployment is either done manually, or as part of the build process. But deployment is a completely different step in your lifecycle. It's important that deployment be automated, but done&#160;separately&#160;from the build process.
<br><excerpt class='endintro'></excerpt><br>
<p>There are two main reasons you should separate your deployment from your build process&#58;</p><ol><li><span style="line-height&#58;20.7999992370605px;">You're not dependent on your servers for your build to succeed. Similarly, if you need to change deployment locations, or add or remove servers, you don't have to edit your build definition and risk breaking your build.<br></span></li><li><span style="line-height&#58;20.7999992370605px;">You want to make sure you're deploying the <strong>*same*</strong>&#160;(tested)&#160;build of your software to each environment. If your deployment step is part of your build step, you may be rebuilding each time you deploy to a new environment.</span></li></ol><div><span style="line-height&#58;20.7999992370605px;">The best tool for&#160;deployments is <a href="http&#58;//octopusdeploy.com/">Octopus Deploy​</a>.</span></div><div><span style="line-height&#58;20.7999992370605px;"><br></span></div><div><img src="/PublishingImages/SugarLearningOctopus.png" alt="SugarLearningOctopus.png" style="margin&#58;5px;width&#58;550px;" /><br></div><dd class="ssw15-rteElement-FigureGood">Figure&#58; Good Example - SSW uses Octopus Deploy to deploy Sugar Learning</dd><div><span style="line-height&#58;20.7999992370605px;"><br></span></div><div><span style="line-height&#58;20.7999992370605px;">Octopus Deploy allows you to package your projects in Nuget packages, publish them to the Octopus server, and deploy&#160;the package to your configured environments. Advanced users can also perform other tasks as part of a deployment like&#160;running&#160;integration and smoke tests, or&#160;notifying&#160;third-party services of a successful deployment.</span></div><div><span style="line-height&#58;20.7999992370605px;"><br></span></div><div><span style="line-height&#58;20.7999992370605px;"><a href="http&#58;//octopusdeploy.com/blog/2.6">Version 2.6 of Octopus Deploy</a> introduced the ability to create&#160;a new release and trigger a deployment when a new package is pushed to the Octopus server. Combined with Octopack, this makes continuous integration very easy from Team Foundation Server.</span></div>


