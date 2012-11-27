---
type: rule
title: Control Choice - Do you use ListView over GridView (was DataGrid) for ReadOnly? (Windows Forms only)
uri: control-choice---do-you-use-listview-over-gridview-was-datagrid-for-readonly-windows-forms-only
created: 2012-11-27T08:50:09.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

 
Yes a ListView looks nicer than a DataGrid, but a Datagrid is better because it has more functionality (out of the box that is). With a ListView you cannot:

- Copy and paste - although you can select a row of data in both controls, you can't copy and paste a whole row from the ListView
- Sort data - always useful when there are more than about 20 rows
- DataBind - always saves heaps of code

   ​
So our old rule was to always use the ugly DataGrid (although we were never happy about that).
<dl class="badImage"><dt><img alt="DataGrid" src="http&#58;//www.ssw.com.au/ssw/Standards/Rules/Images/UsingDataGridWhenNotNeeded.gif" width="534" height="526"></dt>
<dd>Figure&#58; Bad Example - The DataGrid is ugly</dd></dl><dl class="goodImage"><dt><img alt="Sortable ListView" src="http&#58;//www.ssw.com.au/ssw/Standards/Rules/Images/SortableListView.gif" width="534" height="526"></dt>
<dd>Figure&#58; Good Example - A beautiful ListView - a nicer look over the datagrid</dd></dl>
So the listview looks nicer? If you are not convinced here is another one:
<dl class="goodImage"><dt><img alt="Datagrid and Listview" src="http&#58;//www.ssw.com.au/ssw/Standards/Rules/Images/DatagridVSListview.gif"></dt>
<dd>Figure&#58; Good Example - The appearance of DataGrid and ListView</dd></dl>
But another issue is how much code to write... For ListView you will need to write a bit of code to fill the list view...
<dl class="badCode"><dt><pre>    this.listView1.Items.Clear(); 
    // stops drawing to speed up the process, draw right at the end. 
    this.listView1.BeginUpdate(); 
    foreach(DataRow dr in this.dataSet11.Tables[0].Rows)
    &#123; 
       ListViewItem lvi = new ListViewItem(new string[] &#123;dr[0].ToString(),dr[1].ToString(),dr[2].ToString()&#125;);
       lvi.Tag = dr; this.listView1.Items.Add(lvi); 
    &#125; 
    this.listView1.EndUpdate();
                        </pre></dt>
<dd>Figure&#58; 8 lines of code to fill a ListView</dd></dl>
But the datagrid is nicer to code... this is because it comes with data binding ability.
<dl class="badCode"><dt><pre>    // bind it in the designer first. 
    this.oleDbDataAdapter1.Fill(this.dataSet11);
                        </pre></dt>
<dd>Figure&#58; One line of code to fill a DataGrid</dd></dl>
But the SSW ListView (included in the [.NET Toolkit](http&#58;//www.ssw.com.au/ssw/NETToolkit/)) is nicer to code with as it comes with data binding ability.
<dl class="goodCode"><dt><pre>    // bind it in the designer first. 
    this.oleDbDataAdapter1.Fill(this.dataSet11);
                        </pre></dt>
<dd>Figure&#58; One line of code to fill the SSW ListView</dd></dl>
So what is this SSW ListView?

It is an inherited control that how we implemented the ListView to give us what MS left out.

- DataBinding
- Sorting


So now the rules are: 
Always use the SSW ListView. 
Exception: Use the DataGrid when: 

- When not read only - i.e.. users will be editing data directly from the cells.
- You need more than 1 column with checkboxes, or the column with checkboxes can't be the first column. E.g.: <dl class="image"><dt><img alt="DataGrid" src="http&#58;//www.ssw.com.au/ssw/Standards/Rules/Images/DataGrid2CheckBoxes.gif"></dt>
<dd>Figure&#58; One place when you choose a DataGrid over a ListView is when you have 2 checkbox fields</dd></dl>


So in summary, if you don't want users to edit the data directly from the cell, and only the first column need checkboxes, then the ListView is always the better choice.


| We have an example of this in the [SSW .NET Toolkit](http&#58;//www.ssw.com.au/ssw/NETToolkit/). |
| --- |




| We have a program called [SSW Code Auditor](http&#58;//www.ssw.com.au/ssw/CodeAuditor/) to check for this rule. |
| --- |



Note: We have a suggestion for Microsoft to improve the [copy and paste format from a gridview](http&#58;//www.ssw.com.au/ssw/Standards/BetterSoftwareSuggestions/MSForm.aspx#DataGridsFormattingonCopy)

