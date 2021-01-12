---
type: rule
archivedreason: 
title: Do you use Open Graph to control how your links are shared?
guid: 50923325-6be7-4209-b29c-0c1f6e0d7421
uri: do-you-use-open-graph-to-control-how-your-links-are-shared
created: 2018-02-16T22:32:29.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
- title: Tiago Araujo
  url: https://ssw.com.au/people/tiago-araujo
related: []
redirects:
- use-open-graph

---

Open Graph is a metadata tag that allows you to control what content shows up when a page is shared on social media networks.

<!--endintro-->

It should be placed on the &lt;head&gt; section of your page. The most used properties are:

&lt;meta property="og:title" content="Your Custom Title" /&gt;
&lt;meta property="og:description" content="Your custom description of the page." /&gt;
&lt;meta property="og:image" content="https://www.YourCustomImage.jpg"/&gt;

::: bad  
![Figure: Bad example - Shared link has no image and the title was "guessed" by LinkedIn](open-graph-bad.jpg)  
:::  

::: good  
![Figure: Good example - Shared link has a nice image and title, both defined via Open Graph tags](opengraph-good.jpg)  
:::  

**Note:** For LinkedIn you might need to add the prefix as following:

&lt;meta<mark>prefix="og: http://ogp.me/ns#"</mark> property='og:title' content="Microsoft Azure | SSW Consulting - Sydney, Brisbane, Melbourne"/&gt;

More information and other properties can be found at [http://ogp.me](http://ogp.me/)
