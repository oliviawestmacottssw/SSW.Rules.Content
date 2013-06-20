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


As per rule ["Do you have separate development, testing and production environment?"](/Management/RulesToSuccessfulProjects/Pages/SeparateDevelopmentTestingAndProductionEnvironment.aspx), it's           better to use different background colors to identify Development, Test and Production           servers. The way to change the default background color is to edit the global.css.aspx           file:



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


          Figure: In C:\Inetpub\wwwroot\\_common\styles\global.css.aspx comment out and change<br>          the reference in yellow so the users know what server they are on<br>        ![Color of CRM Development Server](/SoftwareDevelopment/RulesToBetterCRMForDevelopers/PublishingImages/CRM_DevelopmentColor.jpg)            Figure: Color of CRM Development Server - Red![Color of CRM Test Server](/SoftwareDevelopment/RulesToBetterCRMForDevelopers/PublishingImages/CRM_TestColor.jpg)            Figure: Color of CRM Test Server - Yellow![Color of CRM Test Server](/SoftwareDevelopment/RulesToBetterCRMForDevelopers/PublishingImages/CRM_ProductionColor.jpg)            Figure: Color of CRM Production Server - Default
In CRM 2011, edit &lt;CrmWebsiteRoot&gt;\\_static\css\1033\cui.css, locate and modify the section ms-cui-tabBody so that it reads:

background-color : #ffffff;

Change color to a suitable color for the environment:

background-color : #bbffaa;

![](/SoftwareDevelopment/RulesToBetterCRMForDevelopers/PublishingImages/CRM2011_ColorCodedRibbon.jpg)

Figure: CRM Ribbon color green to signify production environment



