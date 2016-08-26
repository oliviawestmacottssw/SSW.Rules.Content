---
type: rule
archivedreason: 
title: Do you avoid using UNCs in HREFs?
guid: 7e117f21-a259-489e-bddc-c63de9d95fbe
uri: do-you-avoid-using-uncs-in-hrefs
created: 2016-08-26T17:56:17.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
related: []
redirects: []

---


Initially, errors of this nature would be picked up in the link checking utility. However, that is not the case because the link checker will not report any problems if you run it locally - which is the normal method. The reason it won't see the problems&#160;is because the link checking utility does not check hard coded links to local servers (e.g. http&#58;//localserver/ssw/Default.aspx). Therefore, it is testing a page that will exist internally, but the page will not exist when uploaded to the web (eg.<a href="https&#58;//www.ssw.com.au/ssw/Redirect/ssw/sswhome.htm">http&#58;//www.ssw.com.au/ssw/Default.aspx</a>). <br>
<br><excerpt class='endintro'></excerpt><br>
<dd class="ssw15-rteElement-FigureBad">​​Bad Example&#58; &lt;a href=&quot;//ant/ssw/LookOut.htm&quot;&gt;<br></dd><dd class="ssw15-rteElement-FigureGood"><strong>Good Example&#58;&#160;&lt;a href=&quot;/ssw/LookOut.htm&quot;&gt; </strong><br></dd>


