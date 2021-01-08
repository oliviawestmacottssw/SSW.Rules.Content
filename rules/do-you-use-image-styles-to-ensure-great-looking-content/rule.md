---
type: rule
archivedreason: 
title: Do you use image styles to ensure great looking content?
guid: ae1ff7c9-9c67-4428-a8e7-5eec7e3c182b
uri: do-you-use-image-styles-to-ensure-great-looking-content
created: 2015-10-13T00:27:47.0000000Z
authors: []
related: []
redirects: []

---

Many people will simply "plonk" an image onto a web page in between or next to a block of text. This interrupts the flow of the page and gives a disjointed, unprofessional impression.

A good technique is to set a CSS style to images. This style will be consistent and easy to be used by any person who might edit the website content.

<!--endintro-->
<dl class="badImage"><dt>
      <img src="imageWithoutStyles.jpg" alt="Image without styles">
   </dt><dd>Figure: Bad Example - The image has no styles</dd></dl><dl class="goodImage"><dt>
      <img src="imageWithStyles.jpg" alt="Image with styles">
   </dt><dd>Figure: Good Example - The image has CSS driven margin, padding, borders</dd></dl>
It's also important to choose the correct semantic formatting for images. Different HTML codes might give the same look and feel, but the best way to add images to your page is using       ,       and       tags.
<dl class="badCode"><dt><pre>    <div class="badImage">
        <img src="Images/imageWithoutStyles.jpg" alt="Image without styles">
        <span>Figure: Bad Example - The image has no styles</span>
    </div>   
                    </pre></dt><dd>Figure: Bad Example - Inserting images and captions inside <div> tags</div></dd></dl><dl class="goodCode"><dt><pre>    <dl class="badImage">
        <dt><img src="Images/imageWithoutStyles.jpg" alt="Image without styles"></dt>
        <dd>Figure: Bad Example - The image has no styles</dd>
    </dl>   
                    </pre></dt><dd>Figure: Good Example - Using the <dl>, <dt> and <dd> tags for images</dd></dl>

</dd></dl>
