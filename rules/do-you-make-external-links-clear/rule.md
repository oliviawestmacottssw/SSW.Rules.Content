---
type: rule
archivedreason: 
title: Do you make external links clear?
guid: d178549e-bdef-4636-8dc7-b3514b360bd0
uri: do-you-make-external-links-clear
created: 2015-02-16T02:21:22.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
- title: Tiago Araujo
  url: https://ssw.com.au/people/tiago-araujo
related: []
redirects: []

---

When creating links, you should follow a few basic rules:

<!--endintro-->

1. If your link is an internal link, then it should navigate within the same window. If the link is external, it should open in a new tab and be visually clear to the user that it will lead them away from the current site, that way it is not a surprise.
2. If a link is to an external site, a <br>       **visual indication** should be provided to the user like this: <br>      [This is a link to another site](http&#58;//www.ssw.com.au/ssw/Redirect/Microsoft/microsoft.htm). <br>      
Figure: Bad example - Without visual indication

:::
is by far the best but try other search engines as well)[http://www.google.com](http&#58;//www.ssw.com.au/ssw/Redirect/Web/Google.htm)Search Engines (
::: greybox

Figure: Good example - With visual indication


:::
 is by far the best but try other search engines as well[http://www.google.com](http&#58;//www.ssw.com.au/ssw/Redirect/Web/Google.htm)Search Engines (
::: greybox
3. External link <br>       **external indicators should be inserted by CSS** as following: <br>          a[href\*="//"]:not([href\*="mysite.com"]):after {              
    content: url(https://www.ssw.com.au/ssw/images/external.gif);              
    padding-left: 4px;
}
Figure: Good example - Icon is added by CSS via a simple declaration


We have a program called     [SSW Code Auditor](http&#58;//www.ssw.com.au/ssw/CodeAuditor/) to check for this rule.
 


### Related Rule <br>      


* [Do you make external links open on a new tab?](/external-links-open-on-a-new-tab)
