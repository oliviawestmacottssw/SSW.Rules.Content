---
type: rule
title: Figures - Do you use the right HTML/CSS code to add images and captions?
uri: figures---do-you-use-the-right-htmlcss-code-to-add-images-and-captions
created: 2014-12-04T20:38:45.0000000Z
authors:
- id: 16
  title: Tiago Araujo
- id: 1
  title: Adam Cogan

---

 
​​Most developers put the image and the caption in a DIV tag. The figure is just a paragraph.​
  

```
<div>
<img alt=""/>
<p>Figure: Caption</p>
</div>
```

  Figure: Bad Example
Instead, you should use &lt;DL&gt;, &lt;DT&gt; (which is the item in the list – in our case an image) and &lt;DD&gt;for a caption. This structure gives semantic meaning to the image and figure.
 

```
<dl class="image"> OR <dl class="badImage"> OR <dl class="goodImage">
<dt><img alt=""/></dt>
<dd>Figure: Caption</dd>
</dl>
```

  Figure: Good Example 
**Note:** &lt;dl&gt; stands for "**definition list**"; &lt;dt&gt; for "**definition term**"; and &lt;dd&gt; for "**definition description**".

### ​Relate Rule


- [Figures - Do you add useful and concise figure text?​​​](/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=810b7dab-f94c-4495-bf88-bb80c3bc9776)


