---
type: rule
title: Do you underline links (and include a rollover)?
uri: do-you-underline-links-and-include-a-rollover
created: 2015-02-16T01:30:13.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 44
  title: Duncan Hunter
- id: 16
  title: Tiago Araujo

---

 
Always make links perfectly clear.
 
It's very important that your links stand out from the background as well as the surrounding text. A solid underline and a contrasting colour is the usually the best choice, but the exact method is not important as long as the end result stands out. A link should not only be discoverable upon accidental hovering.

Rollovers are important as they offer visual feedback to a user that this link that will take them somewhere. While there are a myriad of ways to do this; you can't go wrong with a simple text colour change.

[Go to SSW](http&#58;//www.ssw.com.au/SSW/Standards/Rules/RulesToBetterWebsitesNavigation.aspx#)
Bad Example: This link is hard to recognize.
[Go to SSW](http&#58;//www.ssw.com.au/SSW/Standards/Rules/RulesToBetterWebsitesNavigation.aspx#)
Good Example: This link is obvious.
​

![good-example-obvious-roll-over.jpg](/WebSites/RulestoBetterWebsitesNavigation/PublishingImages/Pages/Do-you-underline-links-and-include-a-rollover/good-example-obvious-roll-over.jpg)
​Good Example: Obvious roll over with a button​
**Example CSS for roll over:**

​​​a:link, a:visited { 
    color: (internal value);
    text-decoration: underline;
    cursor: auto;
}​

​​​​​​Figure: Example CSS for roll over ​effect
 SSW has two programs called  [SSW Code Auditor](http&#58;//www.ssw.com.au/ssw/CodeAuditor/Rules.aspx#BreadCrumbs)   [SSW Link Auditor​](https&#58;//sswlinkauditor.com/) to check for this rule.  
