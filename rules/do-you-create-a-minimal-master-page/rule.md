---
type: rule
archivedreason: 
title: Do you create a minimal master page?
guid: 591f621f-a7fb-4ff3-b86d-4ca3fbc085e1
uri: do-you-create-a-minimal-master-page
created: 2009-06-18T06:46:53.0000000Z
authors:
- id: 8
  title: John Liu
- id: 18
  title: Jay Lin
related: []
redirects: []

---

To create a master page or reuse an existing master page is a time-consuming process. Because you have to determine what the Office SharePoint Server 2007 page model requires — necessary content placeholders and controls to work with the page layouts.

 Another problem of Default.master is that it contains many tables that are difficult to style.  
<!--endintro-->
    &lt;%@Master language="C#"%&gt;&lt;/HTML&gt;
&lt;/BODY&gt;
&lt;asp:ContentPlaceHolder id="PlaceHolderTitleAreaClass" runat="server"/&gt;
&lt;asp:ContentPlaceHolder id="PlaceHolderBodyAreaClass" runat="server"/&gt;
&lt;asp:ContentPlaceHolder id="PlaceHolderUtilityContent" runat="server"/&gt;
&lt;/form&gt;
...
&lt;/asp:ContentPlaceHolder&gt;
...
&lt;asp:ContentPlaceHolder id="PlaceHolderFormDigest" runat="server"&gt;
&lt;/table&gt;
&lt;/tr&gt;
&lt;/td&gt;
&lt;/table&gt;
...
<font style="background-color&#58;#ffff80;">&lt;table width=&quot;100%&quot; height=&quot;100%&quot; cellspacing=&quot;0&quot; cellpadding=&quot;0&quot;&gt;</font>
&lt;td&gt;
&lt;tr height="100%"&gt;
&lt;/tr&gt;
&lt;/td&gt;
&lt;/asp:ContentPlaceHolder&gt;
...
&lt;asp:ContentPlaceHolder id="PlaceHolderTopNavBar" runat="server"&gt;
&lt;td id="onetIdTopNavBarContainer" WIDTH=100% class="ms-bannerContainer"&gt;
&lt;tr&gt;
&lt;/tr&gt;
...
&lt;tr&gt;
&lt;/tr&gt;
&lt;/td&gt;
&lt;/asp:ContentPlaceHolder&gt;
&lt;/table&gt;
...
<font style="background-color&#58;#ffff80;">&lt;table CELLPADDING=0 CELLSPACING=0 BORDER=0 WIDTH=&quot;100%&quot;&gt;</font>
&lt;asp:ContentPlaceHolder id="PlaceHolderGlobalNavigation" runat="server"&gt;
&lt;td&gt;
&lt;tr&gt;
<font style="background-color&#58;#ffff80;">&lt;table class=&quot;ms-main&quot; CELLPADDING=0 CELLSPACING=0 BORDER=0 WIDTH=&quot;100%&quot; HEIGHT=&quot;100%&quot;&gt;</font>
&lt;WebPartPages:SPWebPartManager id="m" runat="Server"/&gt;
&lt;form runat="server" onsubmit="return \_spFormOnSubmitWrapper();"&gt;
&lt;BODY scroll="yes” ... &gt;
&lt;/HEAD&gt;
...
&lt;/Title&gt;
&lt;asp:ContentPlaceHolder id=PlaceHolderPageTitle runat="server"/&gt;
&lt;Title ID=onetidTitle&gt;
...
&lt;HEAD runat="server"&gt;
...
Bad example - using default master page 
So we recommend using the minimal master page which includes the necessary placeholders.
To create a minimal master page

1. Open SharePoint Designer.
2. On the File menu, click New, point to SharePoint Content, and then click the Page tab.
3. Double-click Master Page to create a new master page.
4. Click Design to show the master page in design view. You should see header and left margin areas and several content placeholders in the master page.
5. Click Code to show the master page in code view.
6. Copy the code into the master page 
SharePoint 2007 - [https://msdn.microsoft.com/en-us/library/office/aa660698(v=office.12).aspx](https&#58;//msdn.microsoft.com/en-us/library/office/aa660698%28v=office.12%29.aspx) 
SharePoint 2010 - [https://msdn.microsoft.com/en-us/library/office/dn205 273.aspx](https&#58;//msdn.microsoft.com/en-us/library/office/dn205273.aspx)
&lt;%@ Master language="C#" %&gt;&lt;/html&gt;
    &lt;/body&gt;
        &lt;/form&gt;
            &lt;/asp:Panel&gt;
                ...
                &lt;asp:ContentPlaceHolder id="PlaceHolderSearchArea" runat="server"/&gt;
            &lt;asp:Panel visible="false" runat="server"&gt;
            &lt;asp:ContentPlaceHolder id="PlaceHolderMain" runat="server" /&gt;
            &lt;/PublishingWebControls:AuthoringContainer&gt;
                &lt;PublishingConsole:Console runat="server" /&gt;
            &lt;PublishingWebControls:AuthoringContainer id="authoringcontrols" runat="server"&gt;
            &lt;PublishingSiteAction:SiteActionMenu runat="server"/&gt;
            &lt;wssuc:Welcome id="explitLogout" runat="server"/&gt;
        &lt;form runat="server" onsubmit="return \_spFormOnSubmitWrapper();"&gt;
    &lt;body onload="javascript:\_spBodyOnLoadWrapper();"&gt;
    &lt;/head&gt;
        &lt;asp:ContentPlaceHolder id="PlaceHolderAdditionalPageHead" runat="server" /&gt;
        &lt;Sharepoint:CssLink runat="server"/&gt;
        &lt;/asp:ContentPlaceHolder&gt;
            &lt;/title&gt;
                &lt;asp:ContentPlaceHolder id="PlaceHolderPageTitle" runat="server" /&gt;
            &lt;title&gt;
        &lt;asp:ContentPlaceHolder runat="server" id="head"&gt;
    &lt;head runat="server"&gt;
    &lt;SharePoint:RobotsMetaTag runat="server"/&gt;
    &lt;WebPartPages:SPWebPartManager runat="server"/&gt;
&lt;html&gt;
...
    Good example - using minimal master page<br>
7. On the File menu, click Save As, provide a unique file name with the .master extension, and then save the file to the master page gallery (/\_catalogs/masterpage) in your site collection.
