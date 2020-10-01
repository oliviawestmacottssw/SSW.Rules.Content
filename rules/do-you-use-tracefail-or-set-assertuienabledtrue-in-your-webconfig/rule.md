---
type: rule
title: Do you use Trace.Fail or set AssertUIEnabled="true" in your web.config?
uri: do-you-use-tracefail-or-set-assertuienabledtrue-in-your-webconfig
created: 2009-05-13T07:16:16.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 17
  title: Ryan Tee

---

Have you ever seen dialogs raised on the server-side? These dialogs would hang the thread they were on, and hang IIS until they were dismissed. In this case, you might use Trace.Fail or set AssertUIEnabled="true" in your web.config. <br> 
See Scott's blog [Preventing Dialogs on the Server-Side in ASP.NET or Trace.Fail considered Harmful](http&#58;//www.hanselman.com/blog/PreventingDialogsOnTheServerSideInASPNETOrTraceFailConsideredHarmful.aspx)
 public static void ExceptionFunc(string strException) 
<br>    { 
<br>        System.Diagnostics.Trace.Fail(strException);
<br>    }
Figure: Never use Trace.Fail &lt;configuration&gt;
<br>       &lt;system.diagnostics&gt;
<br>          &lt;assert AssertUIEnabled="true" logfilename="c:\log.txt" /&gt;
<br>       &lt;/system.diagnostics&gt;
<br>    &lt;/configuration&gt;
Figure: Never set AssertUIEnabled="true" in web.config &lt;configuration&gt;
<br>       &lt;system.diagnostics&gt;
<br>          &lt;assert AssertUIEnabled="false" logfilename="c:\log.txt" /&gt;
<br>       &lt;/system.diagnostics&gt;
<br>    &lt;/configuration&gt;
Figure: Should set AssertUIEnabled="false" in web.config
