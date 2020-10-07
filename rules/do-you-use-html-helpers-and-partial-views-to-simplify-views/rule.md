---
type: rule
title: Do you use Html Helpers and Partial Views to simplify Views?
uri: do-you-use-html-helpers-and-partial-views-to-simplify-views
created: 2013-03-07T18:47:43.0000000Z
authors:
- id: 23
  title: Damian Brady

---

Repeated sections of User Interface should be encapsulated in either Html Helpers or Partial Views to avoid repetition.
 
[greyBox] 

```
<div class="featured">
    @if (ViewData.ContainsKey("FeaturedProduct"))
    {
        <span class="ProductName">@ViewBag.FeaturedProduct.Name</span>
        <span class="ProductPrice">@ViewBag.FeaturedProduct.Price</span>
    }
</div>
```

 [/greyBox]
Figure: Bad Example – The above code could be encapsulated into a Partial View for reuse
[greyBox] 

```
public static class DateExtensions
{
    public static MvcHtmlString GetTodayDate(this System.Web.Mvc.HtmlHelper helper)
    {
        return new MvcHtmlString(DateTime.Now.ToShortDateString());
    }
}
@Html.GetTodayDate()
```

 [/greyBox]
Figure: Good Example – Using an HTML Helper extension method for reusable code
[greyBox] 

```
@Html.Partial("_FeaturedProduct")
```

 [/greyBox]
Figure: Good Example – Using a Partial View for reusable sections of UI
