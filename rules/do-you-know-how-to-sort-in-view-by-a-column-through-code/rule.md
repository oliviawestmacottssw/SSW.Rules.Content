---
type: rule
title: Do you know how to sort in view by a column through code
uri: do-you-know-how-to-sort-in-view-by-a-column-through-code
created: 2013-07-08T05:40:10.0000000Z
authors:
- id: 9
  title: William Yin
- id: 34
  title: Brendan Richards

---

 ​You may know that it is quite easy to sort view by a column through the UI.![SortInView.png](/SoftwareDevelopment/RulesToBetterSharePoint/PublishingImages/SortInView.png)

But when you are trying to do that via code, you may find a pretty tricky issue.
   You can use some code like:

view.Query = "&lt;OrderBy&gt;&lt;FieldRef Name=\"Modified\" Ascending=\"**FALSE**\" /&gt;&lt;/OrderBy&gt;";

but the below code won't work:



view.Query = "&lt;OrderBy&gt;&lt;FieldRef Name=\"Modified\" Ascending=\"**False**\" /&gt;&lt;/OrderBy&gt;";

​


The full code should be some code ​like:


SPView view = list.DefaultView;
view.Query = "&lt;OrderBy&gt;&lt;FieldRef Name=\"Modified\" Ascending=\"**FALSE**\" /&gt;&lt;/OrderBy&gt;";
view.Update();​​​​
​
​



                   

                    

                    



