---
type: rule
archivedreason: 
title: Do you use Trace.Fail or set AssertUIEnabled="true" in your web.config?
guid: 0fa5857a-6394-471e-ac85-ba2afe055193
uri: do-you-use-tracefail-or-set-assertuienabledtrue-in-your-webconfig
created: 2009-05-13T07:16:16.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
- title: Ryan Tee
  url: https://ssw.com.au/people/ryan-tee
related: []
redirects: []

---


This field should not be null (Remove me when you edit this field).
<br><excerpt class='endintro'></excerpt><br>
<p>See Scott's blog <a href="http&#58;//www.hanselman.com/blog/PreventingDialogsOnTheServerSideInASPNETOrTraceFailConsideredHarmful.aspx">Preventing Dialogs on the Server-Side in ASP.NET or Trace.Fail considered Harmful</a> </p>
<dl class="badCode">
<dt>&#160;public static void ExceptionFunc(string strException) <br>&#123; <br>&#160;&#160;&#160; System.Diagnostics.Trace.Fail(strException);<br>&#125;<br>
<dd>Figure&#58; Never use Trace.Fail </dd></dl>
<dl class="badCode">
<dt>&lt;configuration&gt;<br>&#160;&#160;&#160;&lt;system.diagnostics&gt;<br>&#160;&#160;&#160;&#160;&#160;&#160;&lt;assert AssertUIEnabled=&quot;true&quot; logfilename=&quot;c&#58;\log.txt&quot; /&gt;<br>&#160;&#160;&#160;&lt;/system.diagnostics&gt;<br>&lt;/configuration&gt;<br>
<dd>Figure&#58; Never set AssertUIEnabled=&quot;true&quot; in web.config </dd></dl>
<dl class="goodCode">
<dt>&lt;configuration&gt;<br>&#160;&#160;&#160;&lt;system.diagnostics&gt;<br>&#160;&#160;&#160;&#160;&#160;&#160;&lt;assert AssertUIEnabled=&quot;false&quot; logfilename=&quot;c&#58;\log.txt&quot; /&gt;<br>&#160;&#160;&#160;&lt;/system.diagnostics&gt;<br>&lt;/configuration&gt;<br>
<dd>Figure&#58; Should set AssertUIEnabled=&quot;false&quot; in web.config </dd></dl>


