---
type: rule
title: Do you know the right way to embed a YouTube video?
uri: do-you-know-the-right-way-to-embed-a-youtube-video
created: 2017-09-11T01:29:34.0000000Z
authors:
- id: 51
  title: Farrukh Khan
- id: 60
  title: Anthony Nguyen

---

When you embed a YouTube video it will increase your page size from 500kbs to 1.5Mb or more, depending on how many videos are embedded on the page.

  
![ A side by side comparison – everyone wants less requests and a smaller page size](video-embed-load-time.png) 

[[badExample]]
| ![ Don’t add embed code directly from YouTube. For more details ](video-embed-bad.png)  
[read "A Better Method for Embedding YouTube Videos on your Website"](https://www.labnol.org/internet/light-youtube-embeds/27941/)
`youtube: https://www.youtube.com/embed/eu0qhzevEXQ`
Figure: Bad example – The evil HTML code 
There is a clever, lightweight way to embed a YouTube video, which Google itself practices on their Google+ pages which reduce it to 15kbs.
All you have to do is, whenever you need to embed a video to a page, add the below tag instead of the YouTube video embed code. (Remember to replace VIDEO\_ID with actual ID of the YouTube video)




Figure: Good example – The good HTML code

**Note: **This script needs to be added at the end of the document:

<br>/\* Light YouTube Embeds by @labnol \*/<br>/\* Web: http://labnol.org/?p=27941 \*/<br>document.addEventListener("DOMContentLoaded",<br>function() {<br>var div, n,<br>v = document.getElementsByClassName("youtube-player");<br>for (n = 0; n < v.length; n++) {<br>div = document.createElement("div");<br>div.setAttribute("data-id", v[n].dataset.id);<br>div.innerHTML = labnolThumb(v[n].dataset.id);<br>div.onclick = labnolIframe;<br>v[n].appendChild(div);<br>}<br>});<br>function labnolThumb(id) {<br>var thumb = '<img src="https://i.ytimg.com/vi/ID/hqdefault.jpg">',<br>play = '<div class="play"></div>';<br>return thumb.replace("ID", id) + play;<br>}<br>function labnolIframe() {<br>var iframe = document.createElement("iframe");<br>var embed = "https://www.youtube.com/embed/ID?autoplay=1";<br>iframe.setAttribute("src", embed.replace("ID", this.dataset.id));<br>iframe.setAttribute("frameborder", "0");<br>iframe.setAttribute("allowfullscreen", "1");<br>this.parentNode.replaceChild(iframe, this);<br>}<br>​

..and this needs to be added in the CSS:



​
