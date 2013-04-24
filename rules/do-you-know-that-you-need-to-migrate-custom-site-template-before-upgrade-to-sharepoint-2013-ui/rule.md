---
type: rule
title: Do you know that you need to migrate 'custom site template' before upgrade to SharePoint 2013 UI?
uri: do-you-know-that-you-need-to-migrate-custom-site-template-before-upgrade-to-sharepoint-2013-ui
created: 2013-04-24T01:37:07.0000000Z
authors:
- id: 3
  title: Eric Phan
- id: 9
  title: William Yin

---

 
If you have “custom site template” for  your site, you can’t upgrade your site to the SharePoint 2013 UI unless you have a site template with the same name ready for new UI.

![missingSiteTemplateError.jpg](/PublishingImages/missingSiteTemplateError.jpg)

Figure:SharePoint will show you an error “Missing Site Templates” that prevents you from upgrading
 
​To fix this issue

1. Upgrade your site template’s **content **files and **definition **XML file to SharePoint 2013 (refer to SharePoint 2013 default site template for details).
2. Package the site template’s **content **files to map location “**{SharePointRoot}\Template\SiteTemplate**”.




> ![siteTemplateStructure.jpg](/PublishingImages/siteTemplateStructure.jpg) 
> 
> 3.Package the site template’s **definition **XML file to map location “**{SharePointRoot}\TEMPLATE\1033\XML**”.






> ![siteTemplateDefinitionFile.jpg](/PublishingImages/siteTemplateDefinitionFile.jpg)
> 4.Deploy the package.



> 5.Try to upgrade to SharePoint 2013 UI again.




