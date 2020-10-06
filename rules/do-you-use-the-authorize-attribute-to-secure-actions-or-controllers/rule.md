---
type: rule
title: Do you use the Authorize attribute to secure actions or controllers?
uri: do-you-use-the-authorize-attribute-to-secure-actions-or-controllers
created: 2013-03-07T18:44:09.0000000Z
authors:
- id: 23
  title: Damian Brady

---

ASP.NET MVC provides the [AuthorizeAttribute](https&#58;//msdn.microsoft.com/en-us/library/system.web.mvc.authorizeattribute.aspx) which ensures there is a logged in user before it will execute an action. You can also provide parameters to restrict actions or controllers to only be accessible to certain roles or users. This is a better solution than checking whether a logged-in user exists in code as the authorisation itself doesn’t need to be repeated.
 
[[greyBox]]
| ```
public ActionResult Delete(string tagName)
{
    if (!Request.RequestContext.HttpContext.User.IsInRole("CanDeleteTags"))
    {
        return new System.Web.Mvc.HttpUnauthorizedResult();
    }
    // delete view
    return View();
}
```


Figure: Bad Example – Checking for an appropriate role in code leads to repetition 
[[greyBox]]
| ```
[Authorize(Roles = "CanDeleteTags")]
public ActionResult Delete(string tagName)
{
    // ...delete tag
    return View();
}
```


Figure: Good Example – Using the Authorize attribute to check for appropriate roles
