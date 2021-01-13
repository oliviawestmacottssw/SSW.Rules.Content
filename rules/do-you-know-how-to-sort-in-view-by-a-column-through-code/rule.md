---
type: rule
archivedreason: 
title: Do you know how to sort in view by a column through code
guid: 19d582ea-4667-4b80-a4a3-3dc5a9e515c3
uri: do-you-know-how-to-sort-in-view-by-a-column-through-code
created: 2013-07-08T05:40:10.0000000Z
authors:
- title: William Yin
  url: https://ssw.com.au/people/william-yin
- title: Brendan Richards
  url: https://ssw.com.au/people/brendan-richards
related: []
redirects: []

---

You may know that it is quite easy to sort view by a column through the UI.![](SortInView.png) **Figure: Change view column sort from web UI** 
But when you are trying to do that via code, you may find a pretty tricky issue.

<!--endintro-->
 You can use some code like:

view.Query = "&lt;OrderBy&gt;&lt;FieldRef Name=\"Modified\" Ascending=\" **FALSE** \" /&gt;&lt;/OrderBy&gt;";
 **Figure: Use code to change view sort** 
but the below code won't work:



view.Query = "&lt;OrderBy&gt;&lt;FieldRef Name=\"Modified\" Ascending=\" **False** \" /&gt;&lt;/OrderBy&gt;";

::: bad
Bad Example - the Ascending attribute is case-sensitive

:::

The full code should be some code like:


SPView view = list.DefaultView;
view.Query = "&lt;OrderBy&gt;&lt;FieldRef Name=\"Modified\" Ascending=\" **FALSE** \" /&gt;&lt;/OrderBy&gt;";
view.Update();

::: good
Good Example - the Ascending attribute is using capital charactors as it is case-sensitive  
:::
