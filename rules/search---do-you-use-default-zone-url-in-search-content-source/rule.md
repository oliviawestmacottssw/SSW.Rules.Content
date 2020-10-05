---
type: rule
title: Search - Do you use default zone URL in search content source
uri: search---do-you-use-default-zone-url-in-search-content-source
created: 2016-05-20T07:29:19.0000000Z
authors:
- id: 15
  title: Mark Liu
- id: 9
  title: William Yin

---

​​Using default zone URL in search content source, it will be automatically convert to the relative URL on the search result.e.g. if a user access  search center via http://projects.ssw.com.au/search, the result will be like http://projects.ssw.com.au/search/xxx. While another user access search center via https://projects.ssw.com.au/search, the result will be https://projects.ssw.com.au​/search/xxx.


![](https-data-source.jpg)Bad example: use https://projects.ssw.com.au
​​

![](http-data-source.jpg)Good example: use http://project.ssw.com.au​
