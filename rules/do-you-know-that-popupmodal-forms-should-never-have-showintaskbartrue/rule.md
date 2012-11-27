---
type: rule
title: Do you know that popup/modal forms should never have ShowInTaskbar=True?
uri: do-you-know-that-popupmodal-forms-should-never-have-showintaskbartrue
created: 2012-11-27T04:22:06.0000000Z
authors: []

---

 
Question: What is wrong with this Picture?
![Modal Form in Taskbar](http&#58;//www.ssw.com.au/ssw/Standards/Rules/Images/ShowInTaskBar.jpg)Figure: Can you tell what is wrong with this Picture?   ​
Answer: The 2 SSW SQL Auditor windows are bad, because one is just a modal form.

Note: We don't check for this in Code Auditor because making a form display as popup, is done at runtime via the ShowDialog method.


```
Dim frm as new frmCustomer frm.ShowDialog
```

Figure: Bad Code
If your form is designed to be used modally (and thus be called using ShowDialog) then ShowInTaskbar should be set to false in the form designer.


```
Dim frm as new frmCustomer frm.ShowInTaskBar = False frm.ShowDialog
```

Figure: Bad Code (because this should be set in the form designer)

```
Dim frm as new frmCustomer frm.ShowDialog
```

Figure: Good Code (ShowInTaskbar is set in the form's InitializeComponents method instead)
