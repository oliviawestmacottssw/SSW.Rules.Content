---
type: rule
title: Do you consider SEO in your AngularJS application?
uri: do-you-consider-seo-in-your-angularjs-application
created: 2014-10-30T23:53:12.0000000Z
authors:
- id: 44
  title: Duncan Hunter
- id: 1
  title: Adam Cogan

---

 Search Engine Optimisation (SEO) with a Single Page Application (SPA) needs consideration like any other Framework to ensure it is SEO friendly. Becuase AngularJS manages your routing and URLs it isimportant to be aware of the differences in making an AngulaarJS SPA SEO friendly.
 


​​How to get your AngularJS Single Page Application (SPA) SEO friendly:





1. Enable html5Mode for AngularJS outing
This will remove the hashtagged-URLs by default for pretty URLS, using the pushState feature newer browsers have, which still falls back to the hashbang method if pushState isn't available.​ To enable html5Mode in AngularJs read more [scotch.io​](http&#58;//scotch.io/quick-tips/js/angular/pretty-urls-in-angularjs-removing-the-hashtag).
2. Creating a sitemap
More information at [sitemap.org](http&#58;//www.sitemaps.org/protocol.html)
3. Enriching your app with meta informations
For more information and a demo see this blog [weluse.de](https&#58;//weluse.de/blog/angularjs-seo-finally-a-piece-of-cake.html).





Note: Since May 2014 Google announced that they're finally crawling javascript making SEO for a SPA simpler. Previouisly your SPA needed to distinguish between normal users and crawlers - and re-route (somehow) to the special crawler-only-endpoints if a bot is requesting the page​.​


