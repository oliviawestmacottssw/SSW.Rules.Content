---
type: rule
archivedreason: 
title: Do you know how to sort in view by a column through code
guid: 19d582ea-4667-4b80-a4a3-3dc5a9e515c3
uri: do-you-know-how-to-sort-in-view-by-a-column-through-code
created: 2013-07-08T05:40:10.0000000Z
authors:
- title: William Yin
  url: https://ssw.com.au/people/william-yin
- title: Brendan Richards
  url: https://ssw.com.au/people/brendan-richards
related: []
redirects: []

---


You may know that it is quite&#160;easy to sort view by a column through the UI.<div><img src="/SoftwareDevelopment/RulesToBetterSharePoint/PublishingImages/SortInView.png" alt="SortInView.png" style="margin&#58;5px;width&#58;650px;" /><br></div><div>But when you are trying to do that via code, you may find a pretty tricky issue.</div>
<br><excerpt class='endintro'></excerpt><br>
You can use some code like&#58;<div><div><span class="ssw-rteStyle-CodeArea">view.Query = &quot;&lt;OrderBy&gt;&lt;FieldRef Name=\&quot;Modified\&quot; Ascending=\&quot;<strong>FALSE</strong>\&quot; /&gt;&lt;/OrderBy&gt;&quot;;</span></div><div>but the below code won't work&#58;<br></div><div><span class="ssw-rteStyle-CodeArea">view.Query = &quot;&lt;OrderBy&gt;&lt;FieldRef Name=\&quot;Modified\&quot; Ascending=\&quot;<strong>False</strong>\&quot; /&gt;&lt;/OrderBy&gt;&quot;;</span><div>​<br></div><div>The full code should be some code&#160;​like&#58;</div><div><span class="ssw-rteStyle-CodeArea" style="font-size&#58;12px;"><span style="font-size&#58;12px;background-color&#58;#eeeeee;">SPView view = list.DefaultView;</span><br><span style="font-size&#58;12px;background-color&#58;#eeeeee;">view.Query = &quot;&lt;OrderBy&gt;&lt;FieldRef Name=\&quot;Modified\&quot; Ascending=\&quot;</span><strong style="font-size&#58;12px;">FALSE</strong><span style="font-size&#58;12px;background-color&#58;#eeeeee;">\&quot; /&gt;&lt;/OrderBy&gt;&quot;;</span><br style="font-size&#58;12px;"><span style="font-size&#58;12px;"></span><span style="font-size&#58;12px;background-color&#58;#eeeeee;">view.Update();​​</span><span style="font-size&#58;12px;background-color&#58;#eeeeee;">​</span>​<br></span><br style="font-size&#58;12px;"><br>​</div><br></div><div>&#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160;</div><div>&#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160;&#160;</div><div>&#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160;&#160;</div><br></div>


