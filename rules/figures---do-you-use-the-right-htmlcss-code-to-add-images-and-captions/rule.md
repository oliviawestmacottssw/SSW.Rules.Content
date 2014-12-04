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

 Most developers (even WordPress) put the image and the caption in a DIV tag. The figure is just a paragraph. 

```
<div>
<img alt=""/>
<p>Figure: Caption</p>
</div>
```

 Figure: Bad Example
Instead, use a figure under the image, using a DL. A DL is a HTML tag that stands for ‘Definition List’. It contains a DT which is the item in the list – in our case an image. A DD (the description of the item). This structure gives the image and the figure, semantic meaning.


```
<dl>
<dt><img alt=""/></dt>
<dd>Figure: Caption</dd>
</dl>
```

 Figure: Good Example​ ​​  
