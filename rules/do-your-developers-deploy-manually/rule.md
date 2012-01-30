---
type: rule
title: Do your developers deploy manually?
uri: do-your-developers-deploy-manually
created: 2012-01-30T18:42:41.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 3
  title: Eric Phan

---

 This field should not be null (Remove me when you edit this field). 
We strongly believe that this process should all be automated and painless. Even the receptionist should be able to make a grammatical change on the website and be able to deploy it.

We use TFS gated check-ins to do the deployment for us. When a developer checks there changes into TFS they are prompted with a gated check-in screen.
![Build screen](/WebSites/RulestoBetterWebsites-Deployment/PublishingImages/deployment1.jpg) Figure: "Build" screen

The developer clicks the "Build changes" button and waits for the build to complete. This process needs to take no longer than 2 minutes as it just makes cranky developers if this takes too long.
 The code is put into a TFS shelf, compiled, had all the unit tests run against the code and then deployed to the internal webserver if successful.

Once this process has completed successfully, the developer will get presented with the ability to "reconcile" their local copy of the files as they have now been successfully checked-in to TFS.
![Build screen](/WebSites/RulestoBetterWebsites-Deployment/PublishingImages/deployment2.jpg) Figure: Click on the "Reconcile" button to update your local files

If the developer does not have Build notifications on there local computer then this step can also be easily performed via the Build Explorer in Visual Studio.
![Build screen](/WebSites/RulestoBetterWebsites-Deployment/PublishingImages/deployment3.jpg) Figure: Right click on your last successful build and choose "Reconcile Workspace"

SSW also queues a build process that deploys the changes to our live Australian live production server.

We then schedule anther build to deploy to the other production  servers the next day. This idea behind this is that there is a one day lag between our Australian and Overseas servers so we have a chance to make any changes if required.
 The process that syncs to our external servers is very quick. Only the changes in TFS since the last deployment are sent. This typically takes under 10 seconds to complete.

We also run a longer weekly build that performs a FTP sync between our internal and external servers. This process inspects every file and will upload new or delete any orphaned files.
 The purpose of this is that it is possible that some files failed to copy or were locked at the time of sync. It also cleans up any log or temporary files on the server. It basically ensures that the website is a total copy of the local server.

