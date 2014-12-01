---
type: rule
title: Do you avoid doing an embedded 'Add'?
uri: do-you-avoid-doing-an-embedded-add
created: 2014-12-01T00:01:42.0000000Z
authors: []

---

 
For any case of 'Add New', choose to open a new window (popup) for entering data.
 
​
<dl class="image"><dt><img alt="The 'Add New' button should open a new form" src="http&#58;//www.ssw.com.au/ssw/Standards/Rules/Images/EmbeddedAdd.jpg" style="margin&#58;5px;"></dt><dd>Figure&#58; The 'Add New' button changes from a view into a data entry form</dd></dl><dl class="badImage"><dt><img alt="The 'Add New' did not open a new form" src="http&#58;//www.ssw.com.au/ssw/Standards/Rules/Images/BadEmbeddedAdd.jpg" style="margin&#58;5px;"></dt><dd>Figure&#58; Bad Example - The 'Add New' button, shown in Figure 1, opened the page in the same window</dd></dl>
It is better to open in a new form, reasons being:

- It is better for the user in terms of clarity. The change of view to data entry form can be a surprise
- It is better to code e.g. if you are using this <br>control in a couple of places you may need to show or hide 'Save' <br>buttons etc. Otherwise, it is a pain to make it behave differently in <br>different contexts.


However, you do need to call back on save and requery it.
                    Use a modal form and requery it (DON'T use JavaScript, instead use the Modal Popup Form Example)
                    An example of this is in Outlook with the 'New' button.
<dl class="goodImage"><dt><img alt="The 'New' opens a new form" src="http&#58;//www.ssw.com.au/ssw/Standards/Rules/Images/GoodEmbeddedAdd.jpg" style="margin&#58;5px;"></dt><dd>Figure&#58; Good Example - the 'New' button in Outlook opens a new form for you to construct your email</dd></dl><dl class="image"><dt><img alt="Adding a new table in SharePoiny" src="http&#58;//www.ssw.com.au/ssw/Standards/Rules/Images/sharepoint-add-table.jpg" style="margin&#58;5px;"></dt><dd>Figure&#58; Adding a table in SharePoint have a popup with dimmed background</dd></dl>
