---
type: rule
title: Do you have a label tag for the fields associated with your input?
uri: do-you-have-a-label-tag-for-the-fields-associated-with-your-input
created: 2014-12-16T18:47:45.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

 
When adding input boxes to collect data, please always have a &lt;label&gt; tag                     associated with your &lt;input&gt; tag to link the labels with their respective                     edit controls. This improves accessibility and gives nice focusing stuff (when you                     click the label).
 

```
<p>
    <label for="EmailAddress">Email Address</label>
    <input id="EmailAddress" type="text"/>
</p>
```


**Tip: **To do this in ASP.NET use the AssociatedControlID parameter on your &lt;asp:Label /&gt;                     controls.


```
<p>
    <asp:Label ID="EmailLabel" runat="server" Text="Email Address" AssociatedControlID="EmailAddress"/>
    <asp:TextBox ID="EmailAddress" runat="server"/>
</p>
```


