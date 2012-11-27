---
type: rule
title: Control Choice - Do you use Checked List Boxes instead of multi-select List Boxes?
uri: control-choice---do-you-use-checked-list-boxes-instead-of-multi-select-list-boxes
created: 2012-11-27T08:53:22.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

 
Multi-select listboxes are the bane of a graphical user interface, they have a number of behavioral quirks that make it difficult for users to get used to them:

- They require users to know that you select more than one entry by holding down the Ctrl key
- They lose all selections if you click in the wrong place.
- You can't tell if a Listbox is single-select or multi-select at first glance.

 Item 1 Item 2 Item 3 Item 4 Item 5 Item 6 Item 7 Item 8 Item 9 Item 10 Figure: Bad Example - List Boxes are impractical - try it and see
**Checked Listboxes** are the ideal alternative. They're much more pleasant to use and are a good deal more intuitive - compare to the list above. Checked Listboxes tell users immediately that they have the ability choose multiple options.

- In ASP.NET, use **System.Web.UI.WebControls.CheckBoxList**. If you're having problems with there being too many items in the list, use a **scrolling DIV**
- In Windows Forms, use **System.Windows.Forms.CheckedListBox**



| Item 1 |
| --- |
| Item 2 |
| Item 3 |
| Item 4 |
| Item 5 |
| Item 6 |
| Item 7 |
| Item 8 |
| Item 9 |
| Item 10 |

Figure: Good Example - The beauty of the CheckListBox in ASP.NET We have a program called [SSW Code Auditor](/ssw/CodeAuditor) to check for this rule.  
