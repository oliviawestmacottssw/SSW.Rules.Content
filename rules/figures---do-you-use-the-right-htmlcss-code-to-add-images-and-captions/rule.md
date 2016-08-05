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

 Most developers put the image and the caption in a DIV tag. The figure is just a paragraph.  

```
<div>
<img alt=""/>
<p>Figure: Caption</p>
</div>
```

  Figure: Bad Example
Instead, you should use &lt;DL&gt;, &lt;DT&gt; (which is the item in the list – in our case an image) and &lt;DD&gt;for caption. This structure gives  semantic meaning to the image and figure.​
 

```
<dl>
<dt><img alt=""/></dt>
<dd>Figure: Caption</dd>
</dl>
```

  Figure: Good Example  **Note:** &lt;dl&gt; stands for "**definition list**"; &lt;dt&gt; for "**definition term**"; and &lt;dd&gt; for "**definition description**".

