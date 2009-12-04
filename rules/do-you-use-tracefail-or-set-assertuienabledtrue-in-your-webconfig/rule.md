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

 This field should not be null (Remove me when you edit this field). 
See Scott's blog [Preventing Dialogs on the Server-Side in ASP.NET or Trace.Fail considered Harmful](http&#58;//www.hanselman.com/blog/PreventingDialogsOnTheServerSideInASPNETOrTraceFailConsideredHarmful.aspx)
 public static void ExceptionFunc(string strException) 
{ 
    System.Diagnostics.Trace.Fail(strException);
}
Figure: Never use Trace.Fail &lt;configuration&gt;
   &lt;system.diagnostics&gt;
      &lt;assert AssertUIEnabled="true" logfilename="c:\log.txt" /&gt;
   &lt;/system.diagnostics&gt;
&lt;/configuration&gt;
Figure: Never set AssertUIEnabled="true" in web.config &lt;configuration&gt;
   &lt;system.diagnostics&gt;
      &lt;assert AssertUIEnabled="false" logfilename="c:\log.txt" /&gt;
   &lt;/system.diagnostics&gt;
&lt;/configuration&gt;
Figure: Should set AssertUIEnabled="false" in web.config 
