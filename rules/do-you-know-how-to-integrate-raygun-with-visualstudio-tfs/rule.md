---
type: rule
archivedreason: 
title: Do you know how to integrate RayGun with VisualStudio/TFS?
guid: cd59e270-70b7-4dd3-9a90-64d2dd5849ea
uri: do-you-know-how-to-integrate-raygun-with-visualstudio-tfs
created: 2016-10-25T17:10:27.0000000Z
authors:
- title: Eric Phan
  url: https://ssw.com.au/people/eric-phan
related: []
redirects:
- how-to-integrate-raygun-with-visualstudio-tfs
- do-you-know-how-to-integrate-raygun-with-visualstudiotfs

---

TFS/VisualStudio.com is the source of truth for product development, so how do you get issues in RayGun into TFS? Thankfully there’s a built in integration that lets you do that. 

<!--endintro-->

1. Under Integrations
2. Select Visual Studio Team Services
3. Connect to your TFS or VisualStudio.com instance



::: ok  
![Figure: Link RayGun with TFS/VisualStudio.com](raygun-integration-tfs-1.png)  
:::

Now under the crash report, you have to option to create a PBI and link it to the crash report.


::: ok  
![Figure: Create a new PBI or link to an existing PBI](raygun-integration-tfs-2.png)  
:::

Now you can see which RayGun create reports have already been added to the backlog.


::: ok  
![Figure: Link RayGun with TFS/VisualStudio.com](raygun-integration-tfs-3.png)  
:::

RayGun is a useful tool to use for your DevOps. Check out our rule “[Do you know how DevOps fits in with Scrum?](/do-you-know-how-devops-fits-in-with-scrum)”
