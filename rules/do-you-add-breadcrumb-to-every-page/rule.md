---
type: rule
title: Do you add breadcrumb to every page?
uri: do-you-add-breadcrumb-to-every-page
created: 2015-02-16T01:46:30.0000000Z
authors: []

---

 
Keep a breadcrumb on every page is necessary. With this navigation tool,  users can easily location themselves and find the targets quickly. But  don't link yourself!
 ![add breadcrumb to the top of the page](http&#58;//www.ssw.com.au/SSW/Standards/Rules/Images/WebsiteLayout_Breadcrumb_1.gif)Figure: The breadcrumb
So every page should have a SiteMapPath Control.
&lt;asp:SiteMapPath ID="SiteMapPath1" runat="server" SiteMapProvider="SiteMapProvider1"/&gt; Figure: SiteMapPath Control (Note: <br>      [Code Auditor](http&#58;//www.ssw.com.au/ssw/redirect/ssw/CodeAuditor.htm) checks for the yellow highlighted text)
