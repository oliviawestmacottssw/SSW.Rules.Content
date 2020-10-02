---
type: rule
title: Do you know how to avoid errors?
uri: do-you-know-how-to-avoid-errors
created: 2018-01-17T22:59:30.0000000Z
authors:
- id: 69
  title: Jean Thirion

---

There are certain features in SharePoint on-premises that are no longer supported with SharePoint Online.

If you migrate using the Sharegate migration tool, you want to have zero errors in their reports. To do so, here are what you should do before considering migration:
 
- Get rid of SharePoint Designer customizations on List form

![](avoid-errors-sp-migration1.png)Bad example: Page customized using SharePoint Designer![avoid-errors-sp-migration2.png](avoid-errors-sp-migration2.png)Good example: Out of the box list view page
Remove unsupported columns such as:

- Publishing HTML
- Publishing Hyperlinks
- Calculated Columns with volatile functions ('Me', 'Today'…)
- Managed Metadata columns on folders
- Get rid of MicroFeed

![](avoid-errors-sp-migration3.png)Bad example: Sharegate migration report shows error if MicroFeed(s) have not been removed
