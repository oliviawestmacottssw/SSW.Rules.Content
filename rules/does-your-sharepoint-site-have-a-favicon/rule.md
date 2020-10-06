---
type: rule
title: Does your SharePoint site have a favicon?
uri: does-your-sharepoint-site-have-a-favicon
created: 2009-04-21T03:40:52.0000000Z
authors:
- id: 8
  title: John Liu
- id: 1
  title: Adam Cogan

---

All websites should be following     [the favicon rule](http&#58;//www.ssw.com.au/ssw/Standards/Rules/RulestoBetterWebsitesGraphics.aspx#Favicon).

A Favicon is a small image file included on nearly all professional developed sites. When a browser hits your web site and a user bookmarks that site then the favicon.ico graphic will be displayed in the browser’s URL/address line upon subsequent visits to that site.
 
Let's see how it's done for SharePoint:

[[greyBox]]
| :::
<br>   
&lt;head runat="server"&gt;        
     &lt;meta name="GENERATOR" content="Microsoft SharePoint"&gt;        
     &lt;meta http-equiv="Content-Type" content="text/html; charset=utf-8"&gt;         
     &lt;!--Placeholder for additional overrides--&gt;        
     &lt;asp:ContentPlaceHolder ID="PlaceHolderAdditionalPageHead" runat="server" /&gt;        
            &lt;link rel="shortcut icon" href="~/Style Library/Images/SSW/Rules/ssw.ico" type="image/x-icon" /&gt;
 &lt;/head&gt;

:::
 **Figure: One line of HTML lets you add your company's icon to  your web page**
