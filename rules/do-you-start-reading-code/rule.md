---
type: rule
title: Do you start reading code?
uri: do-you-start-reading-code
created: 2012-03-20T03:46:01.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 24
  title: Adam Stephensen
- id: 23
  title: Damian Brady

---

 *“Aim for simplicity. I want to code to read like poetry”*– Terje Sandstrom 
**Good code:** 

- Is clear and easy to read
- Has consistent and meaningful names for everything
- Has no repeated or redundant code
- Includes comments that explain the intent (the why rather than the what)
- Has consistent styles and formatting


**Tip: **Read this book [Clean Code: A Handbook of Agile Software Craftsmanship](http&#58;//www.google.com.hk/url?sa=t&amp;rct=j&amp;q=clean+code+download&amp;source=web&amp;cd=2&amp;ved=0CDgQFjAB&amp;url=http&#58;//www.e-reading.org.ua/bookreader.php/134601/Clean_Code_-_A_Handbook_of_Agile_Software_Craftsmanship.html&amp;ei=2jRoT8yfM_LSiAKK9piWBw&amp;usg=AFQjCNEGQx__eAf7t0yM_dYGtaaxJ6TqJA) by Robert. C. Martin

**Good code is declarative:**

For example, I want to show all the products where the unit price less than 20, and also how many products are in each category.


Dictionary&lt;string, Grouping&gt; groups = new Dictionary&lt;string, Grouping&gt;();
foreach (Product p in products)
{
    if (p.UnitPrice &gt;= 20)
    {
        if (!groups.ContainsKey(p.CategoryName))
        {
            Grouping r = new Grouping();
            r.CategoryName = p.CategoryName;
            r.ProductCount = 0;
            groups[p.CategoryName] = r;
        }
        groups[p.CategoryName].ProductCount++;
    }
}

List&lt;Grouping&gt; result = new List&lt;Grouping&gt;(groups.Values);
result.Sort(delegate(Grouping x, Grouping y)
{
    return
        x.ProductCount &gt; y.ProductCount ? -1 :
        x.ProductCount &lt; y.ProductCount ? 1 :
        0;
});



```
Figure: Bad example - Not using LINQ. The yellow gives it away.
```



```
Tip: Resharper can automatically convert this code.
```



```
result = products
    .Where(p => p.UnitPrice >= 20)
    .GroupBy(p => p.CategoryName)
    .OrderByDescending(g => g.Count())
    .Select(g => new { CategoryName = g.Key, ProductCount = g.Count() });
```


**Figure: Good example - using LINQ**

**
**

**Tip: **For more information on why declarative programming (aka LINQ, SQL, HTML) is great, watch the [TechDays 2010 Keynote by Anders Hejlsberg.](http&#58;//channel9.msdn.com/blogs/adebruyn/techdays-2010-developer-keynote-by-anders-hejlsberg) Anders explains why it's better to have code "tell what, not how"

**Clean front-end code - HTML**

Anyone who creates their own HTML pages today should aim to make their markup semantically correct.([http://www.webdesignfromscratch.com/html-css/semantic-html/](http&#58;//www.webdesignfromscratch.com/html-css/semantic-html/))

For example, &lt;p&gt; is for a paragraph, not for defining a section. &lt;b&gt; is for bolding, not for emphasizing (&lt;strong&gt; and &lt;em&gt;) do that.




**Clean front-end code - JavaScript**

Clean code and consistent coding standards is not just for server-side code.  It is important that you apply your coding standards to your client-side JavaScript code as well.

You should use a framework like jQuery to make development easier.  jQuery also contributes to clean and consistent code as you don't need to explicitly code for different browsers and standards.

 



```
var ajax;
```



```
if (window.XMLHttpRequest) {
    ajax=new XMLHttpRequest()
} else {
    ajax=new ActiveXObject("Microsoft.XMLHTTP");
}
ajax.onreadystatechange = function() {
    // handle response
}
```



```
ajax.open("GET", uri, true);
```



**Figure: Bad Example - This code doesn't use jQuery**

 




```
$.ajax({
```



```
type: "GET",
```



```
url: uri
```



```
}).done(function (html) {
```



```
$('results').append(html);
```



```
});
```




**Figure: Good Example ****- using jQuery​, the code is much cleaner and easier to read**

