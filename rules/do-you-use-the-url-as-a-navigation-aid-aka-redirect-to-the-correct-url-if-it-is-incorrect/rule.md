---
type: rule
title: Do you use the URL as a navigation aid (aka redirect to the correct url if it is incorrect)?
uri: do-you-use-the-url-as-a-navigation-aid-aka-redirect-to-the-correct-url-if-it-is-incorrect
created: 2013-03-26T20:26:11.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 23
  title: Damian Brady

---

 
MVC gives us great URLs, but you need to help users navigate via the URL.  If the user changes a URL, and the route parameters no longer match, you should correct them with a redirect.
 

```
public ActionResult Edit(string employeename, int id)
{
    var model = _repository.GetEmployee(id);

    // check for a parameter match and redirect if incorrect
    if (string.IsNullOrEmpty(employeename) || employeename != model.EmployeeName)
    {
        return RedirectToAction(
            "Edit", new { employeename = model.EmployeeName, id });
    }

    return View(model);
}
```

Figure: Good example - the comment says it all
