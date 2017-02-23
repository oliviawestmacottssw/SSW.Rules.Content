---
type: rule
title: Controls - Do you make the selected/enabled rows stand out in a datagrid?
uri: controls---do-you-make-the-selectedenabled-rows-stand-out-in-a-datagrid
created: 2012-11-27T09:19:10.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

 
Many times you allow a multiple selection in a grid by using a checkbox. When you do this make it easy to see the distinction of a row that is selected and one that is not. Make it subtle by dimming the unselected text.
   ​  ![Seleted rows not standard out](http&#58;//www.ssw.com.au/ssw/Standards/Rules/Images/Interface_Selected_Rows_Bad.JPG) Figure: Bad Example - Selected rows are not separate from others. ![Seleted rows standard out](http&#58;//www.ssw.com.au/ssw/Standards/Rules/Images/Interface_Selected_Rows_Good.JPG) Figure: Good Example - Selected rows are separate from others.
To make this effect in datagrid, you may need to edit the **cellcontentclick** event handler code. 
Example:

private void DatagridviewRules\_CellContentClick(object sender, DataGridViewCellEventArgs e)
 {
 if (DatagridviewRules.Columns[e.ColumnIndex] is DataGridViewCheckBoxColumn && e.ColumnIndex == 0 &&
e.RowIndex != -1)
 {
 bool boolCheckBox = (bool)(DatagridviewRules.Rows[e.RowIndex].Cells[e.ColumnIndex].Value);
 DatagridviewRules.Rows[e.RowIndex].DefaultCellStyle.ForeColor = boolCheckBox
 ? SystemColors.WindowText
 : SystemColors.ControlDark;
 DataRowView objDataRowView = (DataRowView)DatagridviewRules.Rows[e.RowIndex].DataBoundItem;
 JobRule.DataTableJobRulesRow objDataRow = (JobRule.DataTableJobRulesRow)(objDataRowView.Row);
 updateRuleIsEnabled(objDataRow.RuleId, boolCheckBox);
 updateSelectAllCheckBox();
 updateRulesCount();
 }
 }
 Setting the ForeColor to different ones, like black and gray, can separate the selected rows from others.
