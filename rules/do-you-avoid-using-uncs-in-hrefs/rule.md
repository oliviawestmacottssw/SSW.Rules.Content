---
type: rule
title: Do you avoid using UNCs in HREFs?
uri: do-you-avoid-using-uncs-in-hrefs
created: 2016-08-26T17:56:17.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

Initially, errors of this nature would be picked up in the link checking utility. However, that is not the case because the link checker will not report any problems if you run it locally - which is the normal method. The reason it won't see the problems is because the link checking utility does not check hard coded links to local servers (e.g. http://localserver/ssw/Default.aspx). Therefore, it is testing a page that will exist internally, but the page will not exist when uploaded to the web (eg.[http://www.ssw.com.au/ssw/Default.aspx](https&#58;//www.ssw.com.au/ssw/Redirect/ssw/sswhome.htm)). 
 ​​Bad Example: &lt;a href="//ant/ssw/LookOut.htm"&gt;
**Good Example: &lt;a href="/ssw/LookOut.htm"&gt; **
