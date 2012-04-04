---
type: rule
archivedreason: 
title: Do you use a logging framework?
guid: 37153c77-e1af-4d82-a200-1ab7fbb6d0b2
uri: do-you-use-a-logging-framework
created: 2012-04-01T09:53:00.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
- title: Damian Brady
  url: https://ssw.com.au/people/damian-brady
- title: Matt Wicks
  url: https://ssw.com.au/people/matt-wicks
related: []
redirects: []

---


<p class="MsoListParagraph"><span lang="EN-AU">Unless you are writing a Console application, any output that uses Console.WriteLine will almost certainly be lost.&#160; You're much better off using Trace.WriteLine.</span></p>
<p class="MsoListParagraph"><span lang="EN-AU">You can create a trace listener to send your Trace.WriteLine statements to the Console if you wish, but you can also redirect them elsewhere if required.&#160; See <a href="http&#58;//msdn.microsoft.com/en-us/library/sk36c28t.aspx">this MSDN article for more information</a>.</span></p>
<p class="MsoListParagraph"><span lang="EN-AU" class="ssw-rteStyle-CodeArea">Console.WriteLine(&quot;Service started&quot;);</span><span class="ssw-rteStyle-FigureBad">&#160;Figure&#58; Bad Example - Using Console.WriteLine to write debug information</span></p>
<p class="MsoListParagraph"><span class="ssw-rteStyle-CodeArea">Trace.WriteLine(&quot;Service started&quot;);</span><span class="ssw-rteStyle-FigureGood">&#160;Figure&#58; Good Example - Using Trace.WriteLine to write debug informatio</span></p>
<br><excerpt class='endintro'></excerpt><br>



