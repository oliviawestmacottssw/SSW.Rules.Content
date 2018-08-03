---
type: rule
title: Do you make external links clear?
uri: do-you-make-external-links-clear
created: 2015-02-16T02:21:22.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 16
  title: Tiago Araujo

---

 
When creating links,​​ you should follow a few basic rules: ​
 
1. If your link is an internal link, then it should navigate within the same window. If the link is external, it should open in a new tab and be visually clear to the user that it will lead them away from the current site, that way it is not a surprise.
2. If a link is to an external site, a <br>      **visual indication** should be provided to the user like this: <br>      [This is a link to another site](http&#58;//www.ssw.com.au/ssw/Redirect/Microsoft/microsoft.htm). <br>      
Search Engines ([http://www.google.com](http&#58;//www.ssw.com.au/ssw/Redirect/Web/Google.htm) is by far the best but try other search engines as well)
Figure: Bad example - Without visual indication
Search Engines ([http://www.google.com](http&#58;//www.ssw.com.au/ssw/Redirect/Web/Google.htm) is by far the best but try other search engines as well
Figure: Good example - With visual indication
3. External link <br>      **external indicators should be inserted by CSS** as following: <br>      
a[href\*="//"]:not([href\*="mysite.com"]):after {              
    content: url(https://www.ssw.com.au/ssw/images/external.gif);              
    padding-left: 4px;
}
Figure: Good example - Icon is added by CSS via a simple declaration


We have a program called     [SSW Code Auditor](http&#58;//www.ssw.com.au/ssw/CodeAuditor/) to check for this rule.
 ​


### Related Rule <br>      


- [Do you make external links open on a new tab?​​](/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=1d8a7afd-9762-4bfd-971c-cacd787c28bb)​




