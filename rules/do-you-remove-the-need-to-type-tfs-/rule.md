---
type: rule
title: Do you remove the need to type “/tfs” ?
uri: do-you-remove-the-need-to-type-tfs-
created: 2015-05-05T19:49:26.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 3
  title: Eric Phan

---

 
Many clients that complain when they type: **tfs.northwind.com **
...and then see ‘Server Error 403 – Forbidden: Access is denied’​

It is not a nice experience that in 2015 the out-of-the-box requirement is still to type "/tfs".
 <dl class="badImage"><dt>​<img src="/PublishingImages/tfs-url-1.jpg" alt="tfs-url-1.jpg" style="width&#58;650px;"></dt><dd>Figure&#58; Bad example - A horrible first experience... did I get the URL wrong? Is the server down?​</dd></dl>
**Note: **The better out-of-the-box experience for Exchange OWA is to type [https://mail.ssw.com.au/](https&#58;//mail.ssw.com.au/)
...and it redirects to     
[https://mail.ssw.com.au/owa/auth/logon.aspx?replaceCurrent=1&url=https%3a%2f%2fmail.ssw.com.au%2fowa%2f](https&#58;//mail.ssw.com.au/owa/auth/logon.aspx?replaceCurrent=1&amp;url=https&#58;//mail.ssw.com.au/owa/).

So fix the nasty out-of-the-box experience.​
<dl class="image"><dt>
      <img src="/PublishingImages/tfs-url-2.png" alt="tfs-url-2.png" style="margin&#58;5px;width&#58;650px;">
   </dt><dd>Figure&#58; Option 1 – This is one way. Include some text to tell devs that they can remove the need for /tfs - on the Application Tier page specify port 80 and an empty Virtual Directory</dd></dl><dl class="image"><dt>
      <img src="/PublishingImages/tfs-url-3.png" alt="tfs-url-2.png" style="margin&#58;5px;width&#58;650px;">
   </dt><dd>Figure&#58; Option 2 – This is another way. In IIS add the redirect to remove the need to type “/tfs” 
      <span class="ssw15-rteStyle-Highlight">(recommended)​​</span></dd></dl>
