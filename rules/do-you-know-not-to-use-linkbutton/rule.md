---
type: rule
archivedreason: 
title: Do you know not to use LinkButton?
guid: d96e7ee3-d0eb-46a6-8177-8d96cac2ca44
uri: do-you-know-not-to-use-linkbutton
created: 2016-09-01T17:57:47.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
related: []
redirects:
- do-not-use-linkbutton

---

If we want to refresh and data bind the same page from client side, we can use the javascript function calls "\_\_doPostBack". We shouldn't fire this post back in LinkButton. Otherwise, there will be an error.

<!--endintro-->

::: ok  
![Figure: Right click the link with \_\_doPostBack event](RightClickLink.gif)  
:::  

::: ok  
![Figure: New window with incorrect URL](PostBack.gif)  
:::  

ASPX:
&lt;asp:Panel runat="server" ID="mUpdatePanel" OnLoad="mUpdatePanel\_Load"&gt;
 &lt;asp:Label runat="server" ID="lblTime" /&gt;
 &lt;br /&gt;
 &lt;asp:GridView ID="gvList" runat="server" AutoGenerateColumns="false"&gt;
 &lt;Columns&gt;
 &lt;asp:BoundField DataField="ID" HeaderText="ID" /&gt;
 &lt;/Columns&gt;
 &lt;Columns&gt;
 &lt;asp:BoundField DataField="Name" HeaderText="Name" /&gt;
 &lt;/Columns&gt;
 &lt;/asp:GridView&gt;
 &lt;br /&gt;
 ID:&lt;asp:TextBox ID="txtID" runat="server"/&gt;
 Name:&lt;asp:TextBox ID="txtName" runat="server"/&gt;
&lt;/asp:Panel&gt;
C#:
protected void mUpdatePanel\_Load(object sender, EventArgs e)
{
 lblTime.Text = DateTime.Now.ToLongTimeString();
 ArrayList mList = (ArrayList)ViewState["List"];
 if (txtName.Text.Length &gt; 0)
 {
 Client mClient = new Client();
 mClient.ID = Int32.Parse(txtID.Text);
 mClient.Name = txtName.Text;
 mList.Add(mClient);
 ViewState["List"] = mList;
 gvList.DataSource = mList;
 gvList.DataBind();
 }
}
 **Sample Code** 
&lt;a href="javascript:\_\_doPostBack('mUpdatePanel','');"&gt;Refresh&lt;/a&gt;


::: bad
Bad Code
:::


&lt;input type="button" onclick="javascript:\_\_doPostBack('mUpdatePanel','');" value="Refresh" /&gt;


::: good
Good Code
:::


We have a program called [SSW Code Auditor](https://www.ssw.com.au/ssw/CodeAuditor/) to check for this rule.
