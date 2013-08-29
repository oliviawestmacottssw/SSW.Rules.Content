---
type: rule
archivedreason: 
title: Never Dispose Objects from SPContext.Current
guid: 4117b350-d8e9-47d3-95a0-f993cd7af6a2
uri: never-dispose-objects-from-spcontextcurrent
created: 2013-08-29T00:36:26.0000000Z
authors:
- title: William Yin
  url: https://ssw.com.au/people/william-yin
- title: Brendan Richards
  url: https://ssw.com.au/people/brendan-richards
related: []
redirects: []

---


<div>Althought disposing&#160;objects in SharePoint is important, but never do it with &quot;Current&quot; objects, as you are not allowed to do it.</div><div><br></div><p class="ssw15-rteElement-CodeArea">using (SPWeb web = SPContext.Current.Site.RootWeb)<br>&#123;<br>&#160;//do something here<br>&#125;</p><div>Figure&#58; using statement is trying to dispose current site object - it will cause exception</div><div><br></div><div>Just simplely use &quot;Current&quot; object directly.</div><p class="ssw15-rteElement-CodeArea">SPWeb web =&#160;SPContext.Current.Site.R​ootWeb​;<br>//do something here</p><div><br></div>
<br><excerpt class='endintro'></excerpt><br>



