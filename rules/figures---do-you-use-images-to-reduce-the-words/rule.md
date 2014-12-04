---
type: rule
title: Figures - Do you use images to reduce the words?
uri: figures---do-you-use-images-to-reduce-the-words
created: 2014-12-04T20:21:31.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 16
  title: Tiago Araujo

---

 
An image is worth a thousand words, it's true. So if you can remove text and replace with an image, do so.

So we need a better way to present an image on our website and it should be easy enough to create a decent look.
 
You then have this pretty white flower with a green stem standing on a water pond. It is beautiful.
Figure: Bad example - Here we have text describing a flower![flower](/WebSites/RulesToBetterWebsitesLayout/PublishingImages/flower.jpg)Figure: Good example - Here we have a picture (could be a screen capture) which avoids a thousand words
What else can you do?

- Use good captions - See <br>      [Do you add useful and bold figure text (aka a caption) to avoid a lot of text over images?](/WebSites/RulesToBetterWebsitesLayout/Pages/add-useful-caption.aspx)
- Use good HTML - See <br>      Do you use the right HTML/CSS code to add the useful figure/caption?


### Technical note for the figure (aka Caption)

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

 Figure: Good Example​ ​  
