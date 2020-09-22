---
type: rule
title: Controls - Do you set row select mode as "FullRowSelect" for DataGridView if it is read only? (Windows Forms Only)
uri: controls---do-you-set-row-select-mode-as-fullrowselect-for-datagridview-if-it-is-read-only-windows-forms-only
created: 2012-11-27T09:17:59.0000000Z
authors: []

---

 
If you use the DataGridView control which is read only, you had better set row select mode as "FullRowSelect". If the data cannot be modified we can let users select the whole row instead of one column.
   ​![without FullRowSelect](../../assets/NoneFullRowSelect.gif)Figure: Bad Example - Row select mode is not "FullRowSelect".![with FullRowSelect](../../assets/FullRowSelect.gif)Figure: Good Example - Row select mode is "FullRowSelect".![Set select mode as FullRowSelect](../../assets/setselectmodefull.gif)Figure: Changed row select mode to FullRowSelect.
What's the next step? It's even better if you enable multiple row selection and copying, see [Do your List Views support multiple selection and copying](http://www.ssw.com.au/ssw/Standards/Rules/RulesToBetterWindowsForms.aspx#ListView) on [Rules to Better Windows Forms Applications](http://www.ssw.com.au/ssw/Standards/Rules/RulesToBetterWindowsForms.aspx).

