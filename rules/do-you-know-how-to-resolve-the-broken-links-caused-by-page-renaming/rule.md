---
type: rule
title: Do you know how to resolve the broken links caused by page renaming?
uri: do-you-know-how-to-resolve-the-broken-links-caused-by-page-renaming
created: 2013-07-25T00:00:22.0000000Z
authors:
- id: 9
  title: William Yin
- id: 34
  title: Brendan Richards

---

 Renaming pages in SharePoint site will cause broken links.
All request to old URL will be responsed with a 404 error.
 
​Basically there are three ways to handle this issue.



- Add a page every time for a rename…. JavaScript to redirect or META tag​
- Use custom 404 page to look at a list in SharePoint, the list contains all the renaming records, the records are automatically maintained via page updating events handler. (We are using this way)
- Wait for MS to fix the problem - support alternative links for a page. (TODO: link to a suggestion)






