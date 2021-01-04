---
type: rule
archivedreason: 
title: Do you use Bundling to package script and css files?
guid: d37d8c4d-b868-4124-93f7-a212d11ed390
uri: do-you-use-bundling-to-package-script-and-css-files
created: 2013-03-08T14:33:01.0000000Z
authors:
- title: Damian Brady
  url: https://ssw.com.au/people/damian-brady
related: []
redirects: []

---

ASP.NET provides a great way to compress and package multiple script files or multiple css files.  Bundling multiple files together results in fewer requests from the client and smaller payloads which leads to much faster render times.

<!--endintro-->

Rather than link to each script or css file individually, use bundling to group many together and get the advantages of minification and versioning out of the box.
<dl class="badImage">&lt;dt&gt;<br><br>::: greybox<br><pre>&lt;link rel=&quot;stylesheet&quot; href=&quot;~/Content/themes/base/jquery.ui.core.css&quot; /&gt;
&lt;link rel=&quot;stylesheet&quot; href=&quot;~/Content/themes/base/jquery.ui.resizable.css&quot; /&gt;
&lt;link rel=&quot;stylesheet&quot; href=&quot;~/Content/themes/base/jquery.ui.selectable.css&quot; /&gt;
&lt;link rel=&quot;stylesheet&quot; href=&quot;~/Content/themes/base/jquery.ui.accordion.css&quot; /&gt;
&lt;link rel=&quot;stylesheet&quot; href=&quot;~/Content/themes/base/jquery.ui.autocomplete.css&quot; /&gt;
&lt;link rel=&quot;stylesheet&quot; href=&quot;~/Content/themes/base/jquery.ui.button.css&quot; /&gt;
&lt;link rel=&quot;stylesheet&quot; href=&quot;~/Content/themes/base/jquery.ui.dialog.css&quot; /&gt;
&lt;link rel=&quot;stylesheet&quot; href=&quot;~/Content/themes/base/jquery.ui.slider.css&quot; /&gt;
&lt;link rel=&quot;stylesheet&quot; href=&quot;~/Content/themes/base/jquery.ui.tabs.css&quot; /&gt;
&lt;link rel=&quot;stylesheet&quot; href=&quot;~/Content/themes/base/jquery.ui.datepicker.css&quot; /&gt;
&lt;link rel=&quot;stylesheet&quot; href=&quot;~/Content/themes/base/jquery.ui.progressbar.css&quot; /&gt;
&lt;link rel=&quot;stylesheet&quot; href=&quot;~/Content/themes/base/jquery.ui.theme.css&quot; /&gt;
</pre><br>:::<br><br>&lt;/dt&gt;<dd>Figure&#58; Bad Example – each reference will be downloaded separately and won’t be compressed</dd></dl><dl class="goodImage">&lt;dt&gt;<br><br>::: greybox<br><pre>Configuration&#58;
public static void RegisterBundles(BundleCollection bundles)
&#123;
        bundles.Add(new StyleBundle(&quot;~/Content/themes/base/css&quot;).Include(
                &quot;~/Content/themes/base/jquery.ui.core.css&quot;,
                &quot;~/Content/themes/base/jquery.ui.resizable.css&quot;,
                &quot;~/Content/themes/base/jquery.ui.selectable.css&quot;,
                &quot;~/Content/themes/base/jquery.ui.accordion.css&quot;,
                &quot;~/Content/themes/base/jquery.ui.autocomplete.css&quot;,
                &quot;~/Content/themes/base/jquery.ui.button.css&quot;,
                &quot;~/Content/themes/base/jquery.ui.dialog.css&quot;,
                &quot;~/Content/themes/base/jquery.ui.slider.css&quot;,
                &quot;~/Content/themes/base/jquery.ui.tabs.css&quot;,
                &quot;~/Content/themes/base/jquery.ui.datepicker.css&quot;,
                &quot;~/Content/themes/base/jquery.ui.progressbar.css&quot;,
                &quot;~/Content/themes/base/jquery.ui.theme.css&quot;));
&#125;

View&#58;
@Styles.Render(&quot;~/Content/themes/base/css&quot;)
</pre><br>:::<br><br>&lt;/dt&gt;<dd>Figure&#58; Good Example – Define a bundle and render it in the view for maximum performance</dd></dl>
