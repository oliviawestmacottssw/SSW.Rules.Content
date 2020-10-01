---
type: rule
title: Controls - Do you include a "select all" checkBox on the top?
uri: controls---do-you-include-a-select-all-checkbox-on-the-top
created: 2012-11-27T08:42:03.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

Do you have checkbox (on the top) that let users select or unselect all checkboxes underneath it? If you have a list of checkboxes, you are going to frustrate users unless you provide an easy way to select all. The best way to achieve this is to have a checkbox at the top.
  ![ Good Example - Hotmail does this ![Gmail](../assets/GmailSelectAll.gif) ](../assets/HotmailSelectAll.gif) 
Private Sub CheckBoxSelectAll\_CheckedChanged(ByVal sender As System.Object, ByVal e As System.EventArgs) \_
Handles CheckBoxSelectAll.CheckedChanged
'Select checkbox in each row
For Each sDataGridViewRow As DataGridViewRow In Me.DataGridViewCustomer.Rows
sDataGridViewRow.Cells(0).Value = Me.CheckBoxSelectAll.Checked
Next
End Sub
Code: Code for selecting all checkboxes in a windows form ![ Select all checkboxes in a web form](../assets/SelectAllCheckBox_Web.jpg) 
<br>function SeleteCheckBox()<br>{ <br>for (var n=0; n < document.form1.elements.length; n++) <br>{<br>if (document.form1.elements[n].type == "checkbox" && document.form1.elements[n].name == "gridview")<br>{<br>document.form1.elements[n].checked = document.getElementById("CheckBoxAll").checked; <br>}<br>}<br>} <br>
 Code: Code for selecting all checkboxes in a web form
We have suggestions for Visual Studio .NET about this at [A top CheckBox to "select all" in windows forms](http://www.ssw.com.au/ssw/Standards/BetterSoftwareSuggestions/MSForm.aspx#SelectAllCheckWindows) and [A top CheckBox to "select all" in web forms.](http://www.ssw.com.au/ssw/Standards/BetterSoftwareSuggestions/MSAjax.aspx#SelectAllCheckWeb)
