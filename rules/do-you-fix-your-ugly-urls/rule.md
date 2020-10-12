---
type: rule
title: Do you fix your ugly URL's?
uri: do-you-fix-your-ugly-urls
created: 2015-11-10T21:02:11.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 83
  title: Camilla Rosa Silva

---

Ugly URL's don't only make it difficult for users to browse your site, they can also impact your Google rankings.

[[greyBox | If you have a nasty URL like this...]]
|  http://www.northwind.com/MyInternalDB/UserDatabase/ProductList.aspx?productname=Access
You should fix it up to look more like this:

[[greyBox | Users could even guess the URL]]
|  http://www.northwind.com/products/access

 
1. Add in Global.asax a route
    protected void Application\_Start(object sender, EventArgs e) 
{ 
//RouteTable and PageRouteHandler are in System.Web.Routing 
RouteTable.Routes.Add("ProductRoute", new Route("products/{productname}", new PageRouteHandler("~/MyInternalDB/UserDatabase/ProductList.aspx.aspx"))); 
}
    **Figure: OK example - create a static route if you only have a few rewrites**
2. Use the URL Rewriting Module for IIS7 

[[goodExample]]
| ![An IIS7 Rewrite is much easier to manage](IIS7Rewrite.jpg)
