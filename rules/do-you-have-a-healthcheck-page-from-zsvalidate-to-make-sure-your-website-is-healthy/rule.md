---
type: rule
title: Do you have a HealthCheck page (from /zsValidate) to make sure your website is healthy?
uri: do-you-have-a-healthcheck-page-from-zsvalidate-to-make-sure-your-website-is-healthy
created: 2016-11-28T18:46:01.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 78
  title: Matt Wicks

---

 
​Websites can be complicated, and a very small mistake can take the whole site down. But there are two different kind of errors, coding errors and deployment errors; coding errors should be picked up by compiling and debugging, while deployment errors should be picked up by HealthCheck page.

Whenever there is a deployment problem, instead of fixing it straight away, we find out what the cause of the problem is and create a HealthCheck test to prevent it happening again. So next time, when the site is down or re-deployed to a new server, we can simply run the HealthCheck page and fix all red crosses then the site should be back online.

Dotnet Core has the ability to add a health checks to your application and can be configured for a variety of real-time monitoring scenarios:

- ​Health probes can be used by container orchestrators and load balancers to check an app's status. For example, a container orchestrator may respond to a failing health check by halting a rolling deployment or restarting a container. A load balancer might react to an unhealthy app by routing traffic away from the failing instance to a healthy instance.
- Use of memory, disk, and other physical server resources can be monitored for healthy status.
- Health checks can test an app's dependencies, such as databases and external service endpoints, to confirm availability and normal functioning.​​

See more at https://docs.microsoft.com/en-us/aspnet/core/host-and-deploy/health-checks?view=aspnetcore-3.1





If you need to add a UI to the health check system - we recommend checking out https://github.com/Xabaril/AspNetCore.Diagnostics.HealthChecks.

It includes NuGet packages that makes it easy to test the health of the lots of different endpoints, and you can push the health check results to different logging platforms e.g. Application Insights, DataDog, etc
 
It also includes UI (which is themable) and the UI supports automatic discovery of k8s services exposing pods that have health checks endpoints. This means, you can benefit from it and avoid registering all the endpoints you want to check and let the UI discover them using the k8s api.
 
Best of all they have a [Release Gate available on the DevOps market place​](https://marketplace.visualstudio.com/items?itemName=luisfraile.vss-services-aspnetcorehealthcheck-extensions) for the release pipelines.



 ​​![ui-branding.png](ui-branding.png)
Figure: Sample Health Page

![timeline.png](timeline.png)
​​Figure: Sample Health of an endpoint being viewed in a timeline i.e. so I can see when was a resource last healthy


#### ​Other products using validation status
![Microsoft summary](status-microsoft.jpg)Figure: Microsoft Live status - <br>      [www.apple.com/au/support/systemstatus/](http://status.mailchimp.com/)![Google Apps summary](status-google.jpg)Figure: Google Apps status - <br>      http://www.google.com/appsstatus![Apple summary](status-apple.jpg)Figure: Apple status - <br>      [status.mailchimp.com](https://www.apple.com/au/support/systemstatus/)![Mailchimp summary](status-mailchimp.jpg)Figure: MailChimp status - <br>      [status.mailchimp.com](http://status.mailchimp.com/)
See     [SSW Rules - Do you have a HealthCheck page to test your website dependencies?](https://www.ssw.com.au/SSW/Standards/Rules/RulesToBetterUnitTests.aspx#HealthCheck)
![check-everything.JPG](check-everything.JPG)Figure: Check everything with care


