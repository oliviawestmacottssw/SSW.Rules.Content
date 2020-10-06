---
type: rule
title: Do you use View Models instead of ViewData?
uri: do-you-use-view-models-instead-of-viewdata
created: 2013-03-07T18:23:38.0000000Z
authors:
- id: 23
  title: Damian Brady

---

MVC provides a ViewData collection in which you can store miscellaneous pieces of information to pass to the View.  It’s also accessible it as a Dynamic object by using the ViewBag.  However, you should avoid using ViewData or ViewBag because it isn’t type-safe and relies on [Magic Strings](http&#58;//en.wikipedia.org/wiki/Magic_string).
 
[[greyBox]]
| ```
public ActionResult Index() {
  ViewData["Message"] = "Some Message";
  return View();
}
 
<h1><%: ViewData["Message"] &></h1>
```


Figure: Bad Example – ViewData being used to pass information to the View isn’t type-safe
[[greyBox]]
| ```
public ActionResult Index() {
  var model = new IndexViewModel();
  model.Message = "Some Message";
  return View();
}
 
<h1><%: Model.Message %></h1>
```


Figure: Good Example – Using a ViewModel is a safer way to pass data
