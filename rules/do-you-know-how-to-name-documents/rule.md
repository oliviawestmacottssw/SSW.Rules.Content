---
type: rule
archivedreason: 
title: Do you know how to name documents?
guid: fd6b589b-9f74-4d95-bc4f-b90b4c349c31
uri: do-you-know-how-to-name-documents
created: 2019-02-26T01:04:10.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
- title: William Yin
  url: https://ssw.com.au/people/william-yin
related: []
redirects: []

---


<p class="ssw15-rteElement-P">When naming documents, use hyphens to separate words to make your files&#160;more easily discoverable.<br></p>
<br><excerpt class='endintro'></excerpt><br>
<p class="ssw15-rteElement-CodeArea" style="width&#58;781.188px;">MonthlyReport.docx<br></p><dd class="ssw15-rteElement-FigureBad">Bad Example&#58; File name doesn't contain any separators between words.<br></dd>A file name without spaces&#160;means that the SharePoint doesn't know where one word ends and the other one begins. This means that searching for 'monthly'&#160;or 'report' would&#160;<strong>not</strong>&#160;find this document.<br>
<p class="ssw15-rteElement-CodeArea" style="width&#58;781.188px;">Monthly Report.docx&#160;<br></p><dd class="ssw15-rteElement-FigureBad">Bad Example&#58; File name uses&#160;a&#160;space to separate words.</dd><p class="ssw15-rteElement-P">As far as SharePoint search goes, this is actually a usable option. What makes&#160;spaces&#160;less-preferable is the fact that the URL to this document will have those spaces escaped with the sequence %20. E.g.&#160;<a href="/Pages/Do-you-know-how-to-use-SharePoint-search.aspx">https&#58;//sharepoint/site/library/Monthly%2 0 Report.docx</a>. URLs with escaped spaces are longer and less human-readable.<br></p><p class="ssw15-rteElement-CodeArea" style="width&#58;781.188px;">Monthly_Report.docx&#160;</p><dd class="ssw15-rteElement-FigureBad">Bad&#160;Example&#58; File name uses an underscore to separate words.</dd><p>As far as SharePoint search goes, an underscore is only a valid word separator in SharePoint Standard or Enterprise, from 2010 onwards. Underscores are not valid word separators for search in SharePoint foundation. Also, sometimes&#160;underscores are less visible to users, for example, when a hyperlink is underlined. When reading a hyperlink that is underlined,&#160;it is oft​en possible for the&#160;user to be mistaken by thinking that the URL contains spaces instead of underscores.&#160;For these reasons it is best to avoid their use in file names and titles.<br></p><p class="ssw15-rteElement-CodeArea" style="width&#58;781.188px;">Monthly-Report.docx&#160;<br></p><dd class="ssw15-rteElement-FigureGood">Good Example&#58; File name uses a hyphen to separate words.</dd><p class="ssw15-rteElement-P">A hyphen is the best&#160;choice, because it&#160;is understood both by humans and all versions of SharePoint search.<br></p><h3 class="ssw15-rteElement-H3">Related Rule<br></h3><ul class="ssw15-rteElement-P"><li><a>Do you know how to use SharePoint search?</a><br></li></ul>

