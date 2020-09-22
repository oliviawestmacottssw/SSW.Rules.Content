---
type: rule
title: Control Choice - Do you use GridView over the CheckedListBox?
uri: control-choice---do-you-use-gridview-over-the-checkedlistbox
created: 2012-11-27T08:43:24.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

 
In Web we have:


- Grids E.g. http://demos.kendoui.com/web/grid/selection.html ![](../../assets/external.gif "You are now leaving SSW")


In Windows Forms we have a CheckedListBox. With a CheckedListBox you cannot:

- Sort data - always useful when there are more than about 20 rows
- Contain much information - can only show one field
- DataBind - always costs heaps of code

   ​​ <dl class="badImage"><dt> <img alt="CheckedListBox" src="../../assets/UsingCheckedListBox.gif"> </dt><dd>Figure: Bad Example - The CheckedListBox is limited</dd></dl><dl class="goodImage"><dt> <img alt="DataGrid" src="../../assets/UsingDataGrid.gif" width="601" height="506"> </dt><dd>Figure: Good Example - The DataGrid can show much more information (and if you use a 3rd Party eg. Telerik, then it can be pretty too)</dd></dl>
In Windows Forms, the code of DataGrid databinding is easier than that of CheckedListBox.
<dl class="badCode"><dt><p>ProductsService.Instance.GetAll(Me.ProductsDataSet1)<br>CheckedListBox1.DataSource = Me.ProductsDataSet1.Tables(0)<br>CheckedListBox1.ValueMember = "ProductID"<br>CheckedListBox1.DisplayMember = "ProductName"<br>For i As Integer = 0 To CheckedListBox1.Items.Count - 1<br>Dim checked As Boolean = CType(ProductsDataSet1.Tables(0).Rows(i)("Discontinued"), Boolean)<br>CheckedListBox1.SetItemChecked(i,checked)<br>Next ​<br></p></dt><dd>Figure: 8 lines of code to fill a CheckedListBox</dd></dl><dl class="goodCode"><dt><p>ProductsService.Instance.GetAll(Me.ProductsDataSet1)</p></dt><dd>Figure: One line of code to fill a DataGrid</dd></dl>
But the CheckedListBox is useful if only one field needs displaying.

