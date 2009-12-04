---
type: rule
title: Do you use TreeView control instead of XML control?
uri: do-you-use-treeview-control-instead-of-xml-control
created: 2009-04-29T06:20:33.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 17
  title: Ryan Tee

---

 This field should not be null (Remove me when you edit this field). 

```
<asp:TreeView ID="TreeView1" runat="server" DataSourceID="siteMapDataSource"
ImageSet="Faq" SkipLinkText =""> 
<ParentNodeStyle Font-Bold="False" /> 
<HoverNodeStyle Font-Underline="True" ForeColor="Purple" />   
<SelectedNodeStyle Font-Underline="True" HorizontalPadding="0px"
VerticalPadding="0px" /> 
<NodeStyle Font-Names="Tahoma" Font-Size="8pt" ForeColor="DarkBlue"
HorizontalPadding="5px" NodeSpacing="0px" VerticalPadding="0px" />
</asp:TreeView>
<asp:SiteMapDataSource ID="siteMapDataSource"  runat="server" />
```

Figure: Good Code - [Use TreeView to represent XML hierarchical data](http&#58;//www.ssw.com.au/Demos/03TreeView/Default.aspx)

```
<asp:Xml ID="Xml1" runat="server" DocumentSource="~/Web.xml"
TransformSource="~/Style.xsl"></asp:Xml>
```

Figure: Bad Code - [Use XML to represent XML document using XSL Transformations](http&#58;//www.ssw.com.au/Demos/03TreeView/XML.aspx)
