---
type: rule
title: Do you identify Development, Test and Production Web Servers by colors?
uri: do-you-identify-development-test-and-production-web-servers-by-colors
created: 2012-12-10T19:42:40.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 69
  title: Jean Thirion

---


​As per rule ["Do you have separate development, testing and production environment?"](/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=ae2ccef9-6cdc-4767-8e5a-e0e3dbf46fe2), it's better to use different background colors to identify Development, Test and Production servers.
![crm staging.png](/PublishingImages/crm%20staging.png)**    Figure: Staging uses blue background**![crm production.png](/PublishingImages/crm%20production.png)**Figure: Production uses red background **


The way to change the default background color is to edit the CRM css files. These changes aren't supported and may be overwritten when CRM Rollups are applied.

### CRM 2015 and CRM 2016


Using theme feature to change the environment color.

![CRM2015Theme.JPG](/PublishingImages/CRM2015Theme.JPG)
  
​  Figure: Changing CRM 2016 UI by using theme feature
### CRM 2013

Edit: **&lt;CrmWebsiteRoot&gt;****\\_controls\navbar\navbar.css**

.navigationControl
{
background-color: #006600;
margin: 0;
z-index: 999;
float: left;
width: 100%;
position: relative;
}
 Figure: Edit the background color to reflect the environment
![crm2013_greenbar.jpg](/PublishingImages/crm2013_greenbar.jpg)
 Figure: CRM 2013 with a green navigation bar        

### CRM 2011 

Edit **&lt;CrmWebsiteRoot&gt;\\_static\css\1033\cui.css**, locate and modify the section ms-cui-tabBody so that it reads:

background-color : #ffffff;

Change color to a suitable color for the environment:

background-color : #bbffaa;

![](/PublishingImages/CRM2011_ColorCodedRibbon.jpg)

Figure: CRM Ribbon color green to signify production environment

### CRM 4 

Edit,** &lt;CrmWebsiteRoot&gt;\****\_common\styles\global.css.aspx**


```
body.stage
            {
                <% if (CrmStyles.IsRightToLeft) { %>
                    dir:rtl;
                <%} %>
                border-top:1px solid #6893cf;
                /* background-color: #d6e8ff; */
                background-color: #ffff00;
                padding: 4px;
                /* background-repeat: repeat-x;
                background-image: url(/_imgs/app_back.gif);
                  */
            }
```

          Figure: In C:\Inetpub\wwwroot\\_common\styles\global.css.aspx comment out and change          the reference in yellow so the users know what server they are on![Color of CRM Development Server](/PublishingImages/CRM_DevelopmentColor.jpg)            Figure: Color of CRM Development Server - Red![Color of CRM Test Server](/PublishingImages/CRM_TestColor.jpg)            Figure: Color of CRM Test Server - Yellow![Color of CRM Test Server](/PublishingImages/CRM_ProductionColor.jpg)            Figure: Color of CRM Production Server - Default




