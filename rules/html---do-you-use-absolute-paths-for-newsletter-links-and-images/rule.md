---
type: rule
title: HTML - Do you use absolute paths for newsletter links and images?
uri: html---do-you-use-absolute-paths-for-newsletter-links-and-images
created: 2018-06-07T21:48:16.0000000Z
authors:
- id: 16
  title: Tiago Araujo

---

Newsletters should always use **absolute** references to all links and images within the HTML. Relative paths don't contain the server information so users see a broken link/image - the outside email application won't find the where the file is.
 
&lt;a href="/ssw/Company/ContactUs.aspx "&gt;&lt;img src="/SSW/images/SSWLogo.png"&gt;&lt;/a&gt;
 Figure: Bad example - using relative paths for both link and image on a newsletter

&lt;a href="https://ssw.com.au​/ssw/Company/ContactUs.aspx "&gt;&lt;img src="https://ssw.com.au/SSW/images/SSWLogo.png"&gt;&lt;/a&gt;
 Figure: Good example - using absolute paths for both link and image on a newsletter

​
