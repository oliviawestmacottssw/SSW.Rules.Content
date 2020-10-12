---
type: rule
title: Do you avoid hardcoding URLs (“../”, “~/”, or “/”) and use Url.Action or Html.ActionLink instead?
uri: do-you-avoid-hardcoding-urls---or--and-use-urlaction-or-htmlactionlink-instead
created: 2013-03-07T18:51:39.0000000Z
authors:
- id: 23
  title: Damian Brady

---

Hardcoding URLs in your View can cause problems if your routes or page names need to change.  Instead, you should always use the Url and Html helpers to refer to different pages in your MVC application.
 

[[badExample]]
|  
| 
| ```
| <a href="/Rule/Create">Create a Rule</a>
| ```
| 
|  
Figure: Bad Example – Hard-coded URLs may lead to broken links if routes change

[[goodExample]]
|  
| 
| ```
| @Html.ActionLink("Create a Rule", "Create", "Rule")
| ```
| 
|  
Figure: Good Example – Use the Url or Html helpers to provide links
