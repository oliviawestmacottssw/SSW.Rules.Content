---
type: rule
title: Do you know the best dependency injection container? (aka Do not waste days evaluating IOC containers)
uri: do-you-know-the-best-dependency-injection-container-aka-do-not-waste-days-evaluating-ioc-containers
created: 2013-02-01T16:43:44.0000000Z
authors:
- id: 24
  title: Adam Stephensen
- id: 1
  title: Adam Cogan
- id: 34
  title: Brendan Richards

---

 
​​​You can waste days evaluating IOC containers. The top ones are quite similar. There is not much in this, but the best ones are StructureMap and AutoFac. At SSW we use Autofac on most projects.

Other excellent DI containers are StructureMap, Ninject and Castle Winsdor. They have weaknesses, some are listed below.
 
Dependency Injection is an essential ingredient to having maintainable solutions. IOC containers make doing dependency injection easier.

When selecting a Dependency Injection container it is worth considering a number of factors such as:

- Ease of use
- Configurability: Fluent API and/or XML Configuration
- Performance (Unless you have a very high traffic application the difference should be minimal)
- NuGet Support (only Ninject is doing a poor job of this) - see image


The top tools all contain comparable functionality. In practice which one you use makes little difference, especially when you consider that your container choice should not leak into your domain model.

**Important:** Unless a specific shortfall is discovered with the container your team uses, you should continue to use the same container across all of your projects, become an expert with it and invest time on building features rather than learning new container implementations.
![](/PublishingImages/ninject.jpg)Figure: Bad Example - The Ninject extension packages are not up-to-date. The Ninject.MVC3 package needs to be used for MVC 4 and the Ninject.Web.WebAPI package does not work with the release version of WebApi, so developers must use the Ninject.Web.WebAPI-RC package instead. Also, Ninject doesn’t work in a medium trust environment. <br>      ​​![IOC Container Performance](http&#58;//www.palmmedia.de/content/blogimages/67b056a5-9da8-40b4-9ae6-0c838cdac180.png)Figure: Good Example - Autofac has a good combination of performance and features as per [http://www.palmmedia.de/blog/2011/8/30/ioc-container-benchmark-performance-comparison​​​](http&#58;//www.palmmedia.de/blog/2011/8/30/ioc-container-benchmark-performance-comparison)
**Note:** Autofac's support for child lifetime containers maybe significant for some:​
[​http://nblumhardt.com/2011/01/an-autofac-lifetime-primer](http&#58;//nblumhardt.com/2011/01/an-autofac-lifetime-primer/)

StructureMap does also support a kind of child container:
[http://codebetter.com/jeremymiller/2010/02/10/nested-containers-in-structuremap-2-6-1/](http&#58;//codebetter.com/jeremymiller/2010/02/10/nested-containers-in-structuremap-2-6-1/)

​![Autofac_web.png](/PublishingImages/Autofac_web.png)
Figure: Good Example - the web / mvc integration package layer for Autofac is developed by the same core Autofac team. Some containers (such as Structure Map) require third-party integration layers​​ ​



### Do you know what to do about ASP.NET core (aka ASP.NET 5) default dependency injection?

​We already know what the [best IOC container is](/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=0aa194e1-2de9-4ed1-b430-444109d65a50), but how does ASP.NET core's default dependency injection comapre?

ASP.NET 5 includes default dependency injection for new Web Apps in the Startup.cs file. This is adequate for simple projects, but not designed to compete with the features of alternatives containers (like AutoFac's convention based registration).

"The default services container provided by ASP.NET 5 provides a minimal feature set and is not intended to replace other containers.​​" - Steve Smith, ([ASP.NET Dependency Injection](http&#58;//docs.asp.net/en/latest/fundamentals/dependency-injection.html))

You can quckly spot this error and any more by using the [SSW Code Auditor​](https&#58;//www.ssw.com.au/ssw/CodeAuditor/).

Here is an example of rewiring the default code to AutoFac with the [SSW's Music Store​](https&#58;//github.com/SSWConsulting/enterprise-musicstore-ui-angular2) app:
![SSW-DependencyInjection-Example-Default-Bad.png](/SiteAssets/do-you-know-the-best-dependency-injection-container-(aka-do-not-waste-days-evaluating-ioc-containers)/SSW-DependencyInjection-Example-Default-Bad.png) ​​​​Figure: Bad Example - ​​The default dependency injection for ASP.NET 5​
​​![SSW-DependencyInjection-Example-Default-Good.png](/SiteAssets/do-you-know-the-best-dependency-injection-container-(aka-do-not-waste-days-evaluating-ioc-containers)/SSW-DependencyInjection-Example-Default-Good.png)​
​​Figure: Good Example - The bad example rewired to utilize​ AutoFac. Red boxes outline the modified code.



#### Further Reading:​

- [Do you use a dependency injection centric architecture?](/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=0a5029a1-dd4f-46d7-9f22-8ab328e7c102)
- [​Do you generate the VS dependency graph?](/Pages/DoYouGenerateTheVSDependencyGraph.aspx)​ ​


