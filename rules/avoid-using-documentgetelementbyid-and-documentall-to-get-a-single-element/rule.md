---
type: rule
archivedreason: 
title: Do you avoid using document.getElementById(id) and document.all(id) to get a single element, instead use selector $(#id)?
guid: 9ddcb98a-a721-4191-af87-3109043184f8
uri: avoid-using-documentgetelementbyid-and-documentall-to-get-a-single-element
created: 2016-11-17T15:17:08.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
related: []
redirects:
- do-you-avoid-using-document-getelementbyidid-and-document-allid-to-get-a-single-element-instead-use-selector-id
- do-you-avoid-using-document-getelementbyid(id)-and-document-all(id)-to-get-a-single-element-instead-use-selector-(id)

---


<p>$(#id) is a selector of jQuery. It gets the single element with the given id.<br></p><p><a href="http&#58;//jquery.com/" target="_blank">jQuery</a>&#160;​is a fast and concise JavaScript Library that simplifies how you traverse HTML documents, handle events, perform animations, and add Ajax interactions to your web pages. jQuery is designed to change the way that you write JavaScript.​<br></p>
<br><excerpt class='endintro'></excerpt><br>
<p>​With jQuery, you can write less code but do more work.<br></p><p class="ssw15-rteElement-CodeArea">&lt;h1 id=&quot;Head1&quot;&gt;Hello&lt;/h1&gt; <br>&lt;script type=&quot;text/javascript&quot; language=&quot;javascript&quot;&gt;<br><span style="font-size&#58;1rem;">&#160; &#160; document.all(&quot;Head1&quot;)</span><span style="font-size&#58;1rem;">.style.color=&quot;red&quot;; <br>&lt;/script&gt;</span></p><dd class="ssw15-rteElement-FigureBad">
Figure - Bad Code​​​
</dd><p class="ssw15-rteElement-CodeArea">&lt;h1 id=&quot;Head1&quot;&gt;Hello&lt;/h1&gt; <br>&lt;script type=&quot;text/javascript&quot; language=&quot;javascript&quot;&gt;​​<br><span style="font-size&#58;1rem;">&#160; &#160; document.getElementById(&quot;Head1&quot;)</span><span style="font-size&#58;1rem;">.style.color=&quot;red&quot;; <br>&lt;/script&gt;</span></p><dd class="ssw15-rteElement-FigureBad">
Figure&#58; Bad Code​
</dd><p class="ssw15-rteElement-CodeArea">&lt;h1 id=&quot;Head1&quot;&gt;Hello&lt;/h1&gt; <br>&lt;script type=&quot;text/javascript&quot; language=&quot;javascript&quot;&gt;<br><span style="font-size&#58;1rem;">&#160; &#160; $(&quot;#Head1&quot;)</span><span style="font-size&#58;1rem;">.css(&quot;color&quot;,&quot;red&quot;); <br>​&lt;/script&gt;</span></p><dd class="ssw15-rteElement-FigureGood">
Figure&#58; Good Code - Using $(&quot;#Head1&quot;)​​​<br></dd>


