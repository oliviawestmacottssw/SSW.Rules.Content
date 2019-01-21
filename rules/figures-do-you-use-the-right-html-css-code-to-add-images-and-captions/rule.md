---
type: rule
archivedreason: 
title: Figures - Do you use the right HTML/CSS code to add images and captions?
guid: f7fc077b-13cc-49e2-a487-06824d5d30af
uri: figures-do-you-use-the-right-html-css-code-to-add-images-and-captions
created: 2014-12-04T20:38:45.0000000Z
authors:
- title: Tiago Araujo
  url: https://ssw.com.au/people/tiago-araujo
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
related: []
redirects: []

---


<p>​​Most developers put the image and the caption in a DIV tag. The figure is just a paragraph.​<br></p>
<br><excerpt class='endintro'></excerpt><br>
<font class="ms-rteCustom-CodeArea"> <pre>&lt;div&gt;
&lt;img alt=&quot;&quot;/&gt;
&lt;p&gt;Figure&#58; Caption&lt;/p&gt;
&lt;/div&gt;
</pre> </font> <span class="ms-rteCustom-FigureBad">Figure&#58; Bad Example</span> 
<p>Instead, you should use &lt;DL&gt;,&#160;&lt;DT&gt; (which is the item in the list – in our case an image) and &lt;DD&gt;for a caption. This structure gives semantic<span style="line-height&#58;20.8px;"> meaning</span> to&#160;the image and&#160;figure. <br></p>
<font class="ms-rteCustom-CodeArea"> <pre>&lt;dl class=&quot;image&quot;&gt; OR &lt;dl class=&quot;badImage&quot;&gt; OR &lt;dl class=&quot;goodImage&quot;&gt;
&lt;dt&gt;&lt;img alt=&quot;&quot;/&gt;&lt;/dt&gt;
&lt;dd&gt;Figure&#58; Caption&lt;/dd&gt;
&lt;/dl&gt;
</pre> </font> <span class="ms-rteCustom-FigureGood">Figure&#58; Good Example </span> 
<p><b>Note&#58;</b>&#160;&lt;dl&gt; stands for &quot;<b>definition list</b>&quot;; &lt;dt&gt; for &quot;<b>definition term</b>&quot;; and &lt;dd&gt; for &quot;<b>definition description</b>&quot;.</p>​<br>


