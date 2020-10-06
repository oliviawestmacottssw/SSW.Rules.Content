---
type: rule
title: Do you use startup tasks in the ~/App_Start folder instead of putting code in Global.asax?
uri: do-you-use-startup-tasks-in-the-app_start-folder-instead-of-putting-code-in-globalasax
created: 2013-03-07T18:37:31.0000000Z
authors:
- id: 23
  title: Damian Brady

---

Adding code to the Application\_Start method in the Global.asax file is the easiest and most straight-forward approach for executing startup logic, however, this code should be encapsulated in static methods outside the Global.asax file. Doing this helps provide cleaner code and encourages proper adherence to the Single Responsibility principle.
 
[[greyBox]]
| :::


```
public class MvcApplication : System.Web.HttpApplication
{
    protected void Application_Start()
    {
        AreaRegistration.RegisterAllAreas();

        routes.IgnoreRoute("{resource}.axd/{*pathInfo}");

        routes.MapRoute(
            name: "Default",
            url: "{controller}/{action}/{id}",
            defaults: new { controller = "Home", action = "Index", id = UrlParameter.Optional }
        );        }
}
```


:::
Figure: Bad Example – Logic is implemented in the Application\_Start method which breaks the Single Responsibility Principle
[[greyBox]]
| :::


```
public class MvcApplication : System.Web.HttpApplication
{
    protected void Application_Start()
    {
        AreaRegistration.RegisterAllAreas();

        WebApiConfig.Register(GlobalConfiguration.Configuration);
        FilterConfig.RegisterGlobalFilters(GlobalFilters.Filters);
        RouteConfig.RegisterRoutes(RouteTable.Routes);
        BundleConfig.RegisterBundles(BundleTable.Bundles);
        AuthConfig.RegisterAuth();
    }
}
```


:::


[[goodExample]]
| ![Startup tasks are called from the Application\_Start method but are located in the App\_Start folder](startup-task.jpg)
