---
type: rule
archivedreason: 
title: Do you use startup tasks in the ~/App_Start folder instead of putting code in Global.asax?
guid: 627126fc-f401-4f79-875d-8cdc5b80b10b
uri: do-you-use-startup-tasks-in-the-app_start-folder-instead-of-putting-code-in-global-asax
created: 2013-03-07T18:37:31.0000000Z
authors:
- title: Damian Brady
  url: https://ssw.com.au/people/damian-brady
related: []
redirects: []

---


<p>Adding code to the Application_Start method in the Global.asax file is the easiest and most straight-forward approach for executing startup logic, however,​ this code should be encapsulated in static methods outside the Global.asax file. Doing this helps provide cleaner code and encourages proper adherence to the Single Responsibility principle.<br></p>
<br><excerpt class='endintro'></excerpt><br>
<dl class="badImage"><dt><div class="greyBox"><pre>public class MvcApplication : System.Web.HttpApplication
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

</pre></div></dt><dd>Figure: Bad Example – Logic is implemented in the Application_Start method which breaks the Single Responsibility Principle</dd></dl><dl class="goodImage"><dt><div class="greyBox"><pre>public class MvcApplication : System.Web.HttpApplication
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
</pre></div><br>
      <img src="startup-task.jpg" alt="" /> </dt><dd>Figure: Good Example – Startup tasks are called from the Application_Start method but are located in the App_Start folder​<br><br></dd></dl>


