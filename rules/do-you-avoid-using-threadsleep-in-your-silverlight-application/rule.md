---
type: rule
title: Do you avoid using Thread.Sleep in your Silverlight application?
uri: do-you-avoid-using-threadsleep-in-your-silverlight-application
created: 2011-05-20T07:34:58.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

​Calling Thread.Sleep on your Silverlight application causes the UI thread to sleep. That means the application is not responsive.
<br>If you want to delay something, you can use a [storyboard](http&#58;//msdn.microsoft.com/en-us/library/system.windows.media.animation.storyboard.aspx). <br> Thread.Sleep(5000); 
<br>this.Dispatcher.BeginInvoke(new Action(() =&gt; 
<br>                            { 
<br>                         //Try to reconnect in the background 
<br>                               Connect.Execute(null); 
<br>                             })); 
<br>Bad: Using Thread.Sleep() causes your Silverlight application to freeze 
<br> 
<br>  
<br>Storyboard sb = new Storyboard() { Duration = TimeSpan.FromSeconds(5) }; 
<br>  
<br>sb.Completed += (ds, de) =&gt; this.Dispatcher.BeginInvoke(new Action(() =&gt; 
<br>                                                                       { 
<br>                                                                          //Try to reconnect in the background 
<br>                                                                         Connect.Execute(null); 
<br>                                                                       })); 
<br>sb.Begin(); 
GOOD: Use a Storyboard with a duration of the delay and once the Storyboard is finished running
