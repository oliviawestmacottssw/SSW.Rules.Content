---
type: rule
title: Do you use dashes in your URLs?
uri: do-you-use-dashes-in-your-urls
created: 2015-11-09T20:51:46.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 16
  title: Tiago Araujo

---

 
​​​For maximum readability and SEO use kebab-case (dashes) in your URLs. ​
 
http://northwind.com/pageonworddocumentation
 Figure: Bad example - No kebab-case in URL 


http://northwind.com/PageOnWordDocumentation
 Fi​gure: Bad example - PascalCase (better readability and still works in small caps, but other people might share it without the MixedCase) 



http://northwind.com/page on word documentation

...will become

 http://northwind.com/page20%on20%word20%documentation
 Figure: Bad example - spaces it will show up in your URL structure as 20%, which is bad for readability and SEO


http://northwind.com/page\_on\_word\_documentation
 Figure: OK​ example - underscored (snake\_case) URLs have good readability but are not recommended by Google


http://northwind.com/page-on-word-documentation
Figure: Good example - kebab-case is recommended by Google


**Note: **this is only for the pages and documents within a website - not for the domain. Domains are bad when they have "-" in them!

Read more on [SEO 101: Hyphens vs. Underscores in URLs](https://www.seomechanic.com/seo-101-hyphens-underscores-_-urls/)

### More info​

You can install the IIS [URL Rewrite Module](http://learn.iis.net/page.aspx/460/using-the-url-rewrite-module/) ![](external.gif "You are now leaving SSW") for IIS7 you can make ugly URL's much more friendly.
![Rewrite the HTML](friendly-url-rule.jpg)Figure: Rewrite both the HTML in the page and the incoming URL's to be friendly
The caveat here is that it will only work if the URL is in the clear on the page.

**Note: **This could only be done with certain links as others are postbacks as well.

​

