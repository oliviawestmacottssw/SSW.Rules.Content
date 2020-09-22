---
type: rule
title: Do you know that popup/modal forms should never have ShowInTaskbar=True?
uri: do-you-know-that-popupmodal-forms-should-never-have-showintaskbartrue
created: 2012-11-27T04:22:06.0000000Z
authors: []

---

 
​Question: What is wrong with this Picture?
<dl class="image"><dt><img alt="Modal Form in Taskbar" src="../../assets/ShowInTaskBar.jpg" width="349" height="60"></dt>
<dd>Figure: Can you tell what is wrong with this Picture?</dd></dl>   ​
Answer: The 2 SSW SQL Auditor windows are bad, because one is just a modal form.

Note: We don't check for this in Code Auditor because making a form display as popup, is done at runtime via the ShowDialog method.
<dl class="badCode"><dt><pre>Dim frm as new frmCustomer frm.ShowDialog</pre></dt> <dd>Figure: Bad Code</dd></dl>
If your form is designed to be used modally (and thus be called using ShowDialog) then ShowInTaskbar should be set to false in the form designer.
<dl class="badCode"><dt><pre>Dim frm as new frmCustomer frm.ShowInTaskBar = False frm.ShowDialog</pre></dt> <dd>Figure: Bad Code (because this should be set in the form designer)</dd></dl> <dl class="goodCode"><dt><pre>Dim frm as new frmCustomer frm.ShowDialog</pre></dt> <dd>Figure: Good Code (ShowInTaskbar is set in the form's InitializeComponents method instead)</dd></dl>
