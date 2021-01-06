---
type: rule
archivedreason: 
title: Do you add attributes to your image HTML?
guid: 99419f1d-c003-449e-ab43-e67acf764527
uri: do-you-add-attributes-to-your-image-html
created: 2015-11-10T18:31:57.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
- title: Tiago Araujo
  url: https://ssw.com.au/people/tiago-araujo
related: []
redirects: []

---

What do you do when you want images to link to your site? In the case of images, Google will look for the "alt" text and factor this into the search results. So when you ask someone else to link to your site with an image you should always add attributes like "alt" and "title" into the code. Here's an example.

<!--endintro-->

Hold the cursor over the image below and see what happens.
<dl class="badImage"><dt>
      <img src="../../assets/SSWLogo.png" data-pin-nopin="true" alt="">
      <p class="ssw15-rteElement-CodeArea"><a href="/ssw/Default.aspx"><br>      <img src="logo.png"><br></a></p></dt><dd>Figure: Bad example - No attributes to the image</dd></dl><dl class="goodImage"><dt>
      <img src="../../assets/SSWLogo.png" data-pin-nopin="true" alt="SSW Logo" title="SSW Logo">
      <p class="ssw15-rteElement-CodeArea"><a href="/ssw/Default.aspx"><br>      <img src="logo.png"><mark>alt="SSW Logo"</mark><mark> title="SSW Logo"</mark> /><br></a></p></dt>
   <dd>Figure: Good example - Search engines will index this text. Scroll over</dd></dl>
