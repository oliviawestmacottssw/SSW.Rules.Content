---
type: rule
archivedreason: 
title: Do you avoid using Thread.Sleep in your Silverlight application?
guid: 5ed4ab0e-4bac-4eba-ac0e-fc087efcd865
uri: do-you-avoid-using-threadsleep-in-your-silverlight-application
created: 2011-05-20T07:34:58.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
related: []
redirects: []

---


Calling Thread.Sleep on your Silverlight application causes the UI thread to sleep. That means the application is not responsive.<br>
If you want to delay something, you can use a <a href="http&#58;//msdn.microsoft.com/en-us/library/system.windows.media.animation.storyboard.aspx">storyboard</a>. 

<br><excerpt class='endintro'></excerpt><br>

  <div class="line alt1">
    <span class="content">
      <span style="margin-left&#58;0px !important;" class="block">
        <code class="plain">
          <font class="ms-rteCustom-CodeArea" size="+0">
            <span class="content">
              <span style="margin-left&#58;0px !important;" class="block">
                <code class="plain">Thread.Sleep(5000); </code>
              </span>
            </span>
<div class="line alt2"><span class="content"><span style="margin-left&#58;0px !important;" class="block"><code class="plain">this.Dispatcher.BeginInvoke(new Action(() =&gt; </code></span></span></div>
<div class="line alt1"><span class="content"><code class="spaces">&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;</code><span style="margin-left&#58;308px !important;" class="block"><code class="plain">&#123; </code></span></span></div>
<div class="line alt2"><span class="content"><code class="spaces">&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;</code><span style="margin-left&#58;336px !important;" class="block"><code class="plain">//</code><code class="keyword">Try</code> <code class="plain">to reconnect in the background </code></span></span></div>
<div class="line alt1"><span class="content"><code class="spaces">&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;</code><span style="margin-left&#58;336px !important;" class="block"><code class="plain">Connect.Execute(null); </code></span></span></div>
<div class="line alt2"><span class="content"><code class="spaces">&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;</code><span style="margin-left&#58;308px !important;" class="block"><code class="plain">&#125;)); </code></span></span></div>
<div class="line alt1"><span class="content"><span style="margin-left&#58;0px !important;" class="block"><code class="plain">Bad&#58; Using Thread.Sleep() causes your Silverlight application to freeze </code></span></span></div>
<div class="line alt2"><span class="content"><span style="margin-left&#58;7px !important;" class="block">&#160;</span></span></div>
<div class="line alt1"><span class="content"><code class="spaces">&#160;</code><span style="margin-left&#58;14px !important;" class="block">&#160;</span></span></div>
<div class="line alt2"><span class="content"><code class="spaces">&#160;</code><span style="margin-left&#58;14px !important;" class="block">&#160;</span></span></div>
<div class="line alt1"><span class="content"><code class="spaces">&#160;</code><span style="margin-left&#58;14px !important;" class="block">&#160;</span></span></div>
<div class="line alt2"><span class="content"><span style="margin-left&#58;0px !important;" class="block"><code class="plain">Storyboard sb = new Storyboard() &#123; Duration = TimeSpan.FromSeconds(5) &#125;; </code></span></span></div>
<div class="line alt1"><span class="content"><code class="spaces">&#160;</code><span style="margin-left&#58;7px !important;" class="block">&#160;</span></span></div>
<div class="line alt2"><span class="content"><span style="margin-left&#58;0px !important;" class="block"><code class="plain">sb.Completed += (ds, de) =&gt; this.Dispatcher.BeginInvoke(new Action(() =&gt; </code></span></span></div>
<div class="line alt1"><span class="content"><code class="spaces">&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;</code><span style="margin-left&#58;504px !important;" class="block"><code class="plain">&#123; </code></span></span></div>
<div class="line alt2"><span class="content"><code class="spaces">&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;</code><span style="margin-left&#58;532px !important;" class="block"><code class="plain">//</code><code class="keyword">Try</code> <code class="plain">to reconnect in the background </code></span></span></div>
<div class="line alt1"><span class="content"><code class="spaces">&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;</code><span style="margin-left&#58;532px !important;" class="block"><code class="plain">Connect.Execute(null); </code></span></span></div>
<div class="line alt2"><span class="content"><code class="spaces">&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;</code><span style="margin-left&#58;504px !important;" class="block"><code class="plain">&#125;)); </code></span></span></div>
<div class="line alt1"><span class="content"><span style="margin-left&#58;0px !important;" class="block"><code class="plain">sb.Begin();&#160;</code></span></span></div>
</font>
<div class="line alt1"><span class="content"><span style="margin-left&#58;0px !important;" class="block"><code class="plain">&#160;</code></span></span><font class="ms-rteCustom-FigureGood" size="+0">GOOD&#58; Use a Storyboard with a duration of the delay and once the Storyboard is finished running </font></div>
</code>
      </span>
    </span>
  </div>



