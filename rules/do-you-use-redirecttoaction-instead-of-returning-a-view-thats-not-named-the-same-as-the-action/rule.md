---
type: rule
title: Do you use RedirectToAction instead of returning a view that’s not named the same as the action?
uri: do-you-use-redirecttoaction-instead-of-returning-a-view-thats-not-named-the-same-as-the-action
created: 2013-03-07T18:33:55.0000000Z
authors:
- id: 23
  title: Damian Brady

---

Returning a view that is named differently to the action confuses the MVC process and can make the code difficult to maintain.
 
In cases where data is posted, if you don't do a redirect and the user hits the refresh/reload button in the browser, the data can be is submitted more than once. This can lead to duplicate data being stored in your database.

Redirecting after posted data has been processed is called the     [Post-Redirect-Get (or PRG) pattern](http&#58;//en.wikipedia.org/wiki/Post/Redirect/Get).

[[greyBox]]
| :::


```
[HttpPost]
public ActionResult Create(CreateModel model)
{
    // ... save to DB, then:
    ViewBag.Message = "Successfully created " + model.Name;
    return View("Success");
}
```


:::
Figure: Bad Example – Returning a different view is misleading and potentially dangerous
[[greyBox]]
| :::


```
[HttpPost]
public ActionResult Create(CreateModel model)
{
    // ... save to DB, then:
    return RedirectToAction("Success", new { message = "Successfully created " + model.Name });
}

public ActionResult Success(string message)
{
    ViewBag.Message = message;
    return View();
}
```


:::
Figure: Good Example – Using the PRG pattern to avoid duplicate data being posted
