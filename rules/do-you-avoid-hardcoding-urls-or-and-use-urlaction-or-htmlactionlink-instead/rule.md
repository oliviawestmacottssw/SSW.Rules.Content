---
type: rule
archivedreason: 
title: Do you avoid hardcoding URLs (“../”, “~/”, or “/”) and use Url.Action or Html.ActionLink instead?
guid: 582c7a84-24ff-40ca-b1ff-332ec3a191a2
uri: do-you-avoid-hardcoding-urls-or-and-use-urlaction-or-htmlactionlink-instead
created: 2013-03-07T18:51:39.0000000Z
authors:
- id: 23
  title: Damian Brady
related: []
redirects: []

---

Hardcoding URLs in your View can cause problems if your routes or page names need to change.  Instead, you should always use the Url and Html helpers to refer to different pages in your MVC application.

<!--endintro-->



:::


```
<a href="/Rule/Create">Create a Rule</a>
```


::: greybox
Figure: Bad Example – Hard-coded URLs may lead to broken links if routes change


:::


```
@Html.ActionLink("Create a Rule", "Create", "Rule")
```


::: greybox
Figure: Good Example – Use the Url or Html helpers to provide links
