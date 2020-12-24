---
type: rule
archivedreason: 
title: Do you know how to sort in view by a column through code
guid: 19d582ea-4667-4b80-a4a3-3dc5a9e515c3
uri: do-you-know-how-to-sort-in-view-by-a-column-through-code
created: 2013-07-08T05:40:10.0000000Z
authors:
- id: 9
  title: William Yin
- id: 34
  title: Brendan Richards
related: []
redirects: []

---

You may know that it is quite easy to sort view by a column through the UI.
![Change view column sort from web UI](SortInView.png)
But when you are trying to do that via code, you may find a pretty tricky issue.

<!--endintro-->
 You can use some code like:

view.Query = "<orderby><fieldref name="\&quot;Modified\&quot;" ascending=""></fieldref> <strong>FALSE</strong> \" /></orderby>";
 **Figure: Use code to change view sort** 
but the below code won't work:



view.Query = "<orderby><fieldref name="\&quot;Modified\&quot;" ascending=""></fieldref> <strong>False</strong> \" /></orderby>";


::: bad
Bad Example - the Ascending attribute is case-sensitive

:::


The full code should be some code like:


SPView view = list.DefaultView;
view.Query = "<orderby><fieldref name="\&quot;Modified\&quot;" ascending=""></fieldref> <strong>FALSE</strong> \" /></orderby>";
view.Update();


::: good
Good Example - the Ascending attribute is using capital charactors as it is case-sensitive
:::
