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

 *“Aim for simplicity. I want to code to read like poetry”*– Terje Sandstrom **​Clean Back-end Code** 
   -Meaningful names

    -Functions

         Prefer exceptions to returning error codes

         don't repeat yourself

   -Comments

   -Fommating

[TODO:reference should be deleted 

&lt;&lt;[Clean Code: A Handbook of Agile Software Craftsmanship](http&#58;//www.google.com.hk/url?sa=t&amp;rct=j&amp;q=clean+code+download&amp;source=web&amp;cd=2&amp;ved=0CDgQFjAB&amp;url=http&#58;//www.e-reading.org.ua/bookreader.php/134601/Clean_Code_-_A_Handbook_of_Agile_Software_Craftsmanship.html&amp;ei=2jRoT8yfM_LSiAKK9piWBw&amp;usg=AFQjCNEGQx__eAf7t0yM_dYGtaaxJ6TqJA)&gt;&gt;-Robert.C.Martin ]




**Clean front-end code - semantics html**

Anyone who creates their own HTML pages today should aim to make their markup semantically correct.([http://www.webdesignfromscratch.com/html-css/semantic-html/](http&#58;//www.webdesignfromscratch.com/html-css/semantic-html/))

&lt;p&gt; is for a paragraph,not for defining a section;&lt;b&gt; is for bolding,not for emphasizing,&lt;strong&gt;,&lt;em&gt; do that.

**
**

**declartive programming(****Question:****s****hould we force to use Linq???)**** - Tell what,not how**[[TechDays 2010 Keynote by Anders Hejlsberg: Trends and future directions in programming ​languages​](http&#58;//channel9.msdn.com/blogs/adebruyn/techdays-2010-developer-keynote-by-anders-hejlsberg)]

 



**e.g.**I want to show some products which unit price less than 20,and also  to know how many  products in every category.

one way to solve the problem:**Tell**** how without Linq**


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
the other way to solve the problem:Tell what with Linq(I can understand the developer's intenstion quickly)
```



```
result = products
    .Where(p => p.UnitPrice >= 20)
    .GroupBy(p => p.CategoryName)
    .OrderByDescending(g => g.Count())
    .Select(g => new { CategoryName = g.Key, ProductCount = g.Count() });
```


**
**

**
**

