---
type: rule
title: Do you have generic exception handler in your Global.asax?
uri: do-you-have-generic-exception-handler-in-your-globalasax
created: 2016-08-25T14:47:18.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

Add your code to handle generic exception of your ASP.NET application in Application\_Error.
 
private static readonly ILog log = LogManager.GetLogger(typeof(MvcApplication));

        protected void Application\_Error(object sender, EventArgs e)
        {
            Exception ex = Server.GetLastError().GetBaseException();
            log.Fatal("Unhandled Exception", ex);
        }
Figure. Exception handler in Global.asax.cs
