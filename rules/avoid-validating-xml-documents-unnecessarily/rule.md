---
type: rule
archivedreason: 
title: Do you avoid validating XML documents unnecessarily?
guid: d65b2247-f519-4257-b304-bb81be2581d6
uri: avoid-validating-xml-documents-unnecessarily
created: 2018-04-25T19:38:17.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
related: []
redirects:
- do-you-avoid-validating-xml-documents-unnecessarily

---


<p>Validating an XML document against a schema is expensive, and should not be done where it is not absolutely necessary. Combined with weight the XML document object, validation can cause a significant performance hit&#58;</p><ul><li>Read with XmlValidatingReader&#58; 172203 nodes - 812 ms</li><li>Read with XmlTextReader&#58; 172203 nodes - 320 ms</li><li>Parse using XmlDocument no validation - length 1619608 - 1052 ms</li><li>Parse using XmlDocument with XmlValidatingReader&#58; length 1619608 - 1862 ms</li></ul><p>You can disable validation when using the XmlDocument object by passing an XmlTextReader instead of the XmlValidatingTextReader&#58;​<br></p>
<br><excerpt class='endintro'></excerpt><br>
<p class="ssw15-rteElement-CodeArea">​XmlDocument report = new XmlDocument();<br> XmlTextReader tr = new XmlTextReader(Configuration.LastReportPath);<br> report.Load(tr);<br></p><p><br>To perform validation&#58;<br></p><p class="ssw15-rteElement-CodeArea">XmlDocument report = new XmlDocument();<br> XmlTextReader tr = new XmlTextReader(Configuration.LastReportPath);<br> XmlValidatingReader reader = new XmlValidatingReader(tr);<br> report.Load(reader);<br></p><p><br>The XSD should be distributed in the same directory as the XML file and a relative path should be used&#58;<br></p><p class="ssw15-rteElement-CodeArea">&lt;Report&gt; &lt;Report xmlns=&quot;LinkAuditorReport.xsd&quot;&gt;<br> ... &lt;/Report&gt;​​<br></p>


