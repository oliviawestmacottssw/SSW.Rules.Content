---
type: rule
archivedreason: 
title: Search - Do you add https by extending web application
guid: aa23853e-3239-4739-bfb5-a01328416962
uri: search-do-you-add-https-by-extending-web-application
created: 2016-05-20T06:51:56.0000000Z
authors: []
related: []
redirects:
- extend-web-application-for-https

---

It is recommended to bind https by extending web applications in central admin site, rather than configuring in IIS

<!--endintro-->
![configurationInIIS.jpg](configurationInIIS.jpg)

::: bad
Bad example: Add https binding in IIS
:::

![extendwebapplication.jpg](extendwebapplication.jpg)

::: good
Good example: Extend web application and assign https to the Internet zone
:::
