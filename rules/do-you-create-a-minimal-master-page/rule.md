---
type: rule
title: Do you create a minimal master page?
uri: do-you-create-a-minimal-master-page
created: 2009-06-18T06:46:53.0000000Z
authors:
- id: 8
  title: John Liu
- id: 18
  title: Jay Lin

---

 To create a master page or reuse an existing master page is a time-consuming process. Because you have to determine what the Office SharePoint Server 2007 page model requires — necessary content placeholders and controls to work with the page layouts.

<br>Another problem of Default.master is that it contains many tables that are difficult to style.<br> &lt;%@Master language="C#"%&gt;
<br>    ...
<br>    &lt;HEAD runat="server"&gt;
<br>    ...
<br>    &lt;Title ID=onetidTitle&gt;
<br>    &lt;asp:ContentPlaceHolder id=PlaceHolderPageTitle runat="server"/&gt;
<br>    &lt;/Title&gt;
<br>    ...
<br>    &lt;/HEAD&gt;
<br>    &lt;BODY scroll="yes” ... &gt;
<br>    &lt;form runat="server" onsubmit="return \_spFormOnSubmitWrapper();"&gt;
<br>    &lt;WebPartPages:SPWebPartManager id="m" runat="Server"/&gt;
&lt;table class="ms-main" CELLPADDING=0 CELLSPACING=0 BORDER=0 WIDTH="100%" HEIGHT="100%"&gt;
<br>    &lt;tr&gt;
<br>    &lt;td&gt;
<br>    &lt;asp:ContentPlaceHolder id="PlaceHolderGlobalNavigation" runat="server"&gt;
&lt;table CELLPADDING=0 CELLSPACING=0 BORDER=0 WIDTH="100%"&gt;
<br>    ...
<br>    &lt;/table&gt;
<br>    &lt;/asp:ContentPlaceHolder&gt;
<br>    &lt;/td&gt;
<br>    &lt;/tr&gt;
<br>    &lt;tr&gt;
<br>    ...
<br>    &lt;/tr&gt;
<br>    &lt;tr&gt;
<br>    &lt;td id="onetIdTopNavBarContainer" WIDTH=100% class="ms-bannerContainer"&gt;
<br>    &lt;asp:ContentPlaceHolder id="PlaceHolderTopNavBar" runat="server"&gt;
<br>    ...
<br>    &lt;/asp:ContentPlaceHolder&gt;
<br>    &lt;/td&gt;
<br>    &lt;/tr&gt;
<br>    &lt;tr height="100%"&gt;
<br>    &lt;td&gt;
&lt;table width="100%" height="100%" cellspacing="0" cellpadding="0"&gt;
<br>    ...
<br>    &lt;/table&gt;
<br>    &lt;/td&gt;
<br>    &lt;/tr&gt;
<br>    &lt;/table&gt;
<br>    &lt;asp:ContentPlaceHolder id="PlaceHolderFormDigest" runat="server"&gt;
<br>    ...
<br>    &lt;/asp:ContentPlaceHolder&gt;
<br>    ...
<br>    &lt;/form&gt;
<br>    &lt;asp:ContentPlaceHolder id="PlaceHolderUtilityContent" runat="server"/&gt;
<br>    &lt;asp:ContentPlaceHolder id="PlaceHolderBodyAreaClass" runat="server"/&gt;
<br>    &lt;asp:ContentPlaceHolder id="PlaceHolderTitleAreaClass" runat="server"/&gt;
<br>    &lt;/BODY&gt;
<br>    &lt;/HTML&gt; Bad example - using default master page 
So we recommend using the minimal master page which includes the necessary placeholders.
 To create a minimal master page

1. Open SharePoint Designer.
2. On the File menu, click New, point to SharePoint Content, and then click the Page tab.
3. Double-click Master Page to create a new master page.
4. Click Design to show the master page in design view. You should see header and left margin areas and several content placeholders in the master page.
5. Click Code to show the master page in code view.
6. Copy the code from [How to: Create a Minimal Master Page](http&#58;//msdn.microsoft.com/en-us/library/aa660698.aspx) into the master page.<br>    &lt;%@ Master language="C#" %&gt;
<br>        ...
<br>        &lt;html&gt;
<br>            &lt;WebPartPages:SPWebPartManager runat="server"/&gt;
<br>            &lt;SharePoint:RobotsMetaTag runat="server"/&gt;
<br>            &lt;head runat="server"&gt;
<br>                &lt;asp:ContentPlaceHolder runat="server" id="head"&gt;
<br>                    &lt;title&gt;
<br>                        &lt;asp:ContentPlaceHolder id="PlaceHolderPageTitle" runat="server" /&gt;
<br>                    &lt;/title&gt;
<br>                &lt;/asp:ContentPlaceHolder&gt;
<br>                &lt;Sharepoint:CssLink runat="server"/&gt;
<br>                &lt;asp:ContentPlaceHolder id="PlaceHolderAdditionalPageHead" runat="server" /&gt;
<br>            &lt;/head&gt;
<br>            &lt;body onload="javascript:\_spBodyOnLoadWrapper();"&gt;
<br>                &lt;form runat="server" onsubmit="return \_spFormOnSubmitWrapper();"&gt;
<br>                    &lt;wssuc:Welcome id="explitLogout" runat="server"/&gt;
<br>                    &lt;PublishingSiteAction:SiteActionMenu runat="server"/&gt; 
<br>                    &lt;PublishingWebControls:AuthoringContainer id="authoringcontrols" runat="server"&gt;
<br>                        &lt;PublishingConsole:Console runat="server" /&gt;
<br>                    &lt;/PublishingWebControls:AuthoringContainer&gt;
<br>                    &lt;asp:ContentPlaceHolder id="PlaceHolderMain" runat="server" /&gt;
<br>                    &lt;asp:Panel visible="false" runat="server"&gt;
<br>                        &lt;asp:ContentPlaceHolder id="PlaceHolderSearchArea" runat="server"/&gt;
<br>                        ...
<br>                    &lt;/asp:Panel&gt;
<br>                &lt;/form&gt;
<br>            &lt;/body&gt;
<br>        &lt;/html&gt;     Good example - using minimal master page
7. On the File menu, click Save As, provide a unique file name with the .master extension, and then save the file to the master page gallery (/\_catalogs/masterpage) in your site collection.


