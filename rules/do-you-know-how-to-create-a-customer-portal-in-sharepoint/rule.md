---
type: rule
title: Do you know how to create a "Customer Portal" (in SharePoint)?
uri: do-you-know-how-to-create-a-customer-portal-in-sharepoint
created: 2009-05-28T06:51:18.0000000Z
authors:
- id: 9
  title: William Yin
- id: 19
  title: Sumesh Ghimire
- id: 1
  title: Adam Cogan

---

 
You should do anything that helps a project. The best thing is to enable great collaboration, by giving your customer an awesome 'Customer Portal'.  Then they can see new mockups, comment on features, get new releases and participate in team discussions on their particular project.

So the first thing you should do is to create a 'Customer Portal' in your SharePoint extranet. Then give your customer a login, send them an email and they are now going to really get involved!

It is advised that you create a customized SharePoint Team Collaboration site template. Then you can very quickly initialize a new site for each new customer.

Then follow these steps to create a customer portal with SharePoint 2007:
 
1. Go to the root where you want to create a site, i.e sharepoint.ssw.com.au
2. Click "Site Actions" on right hand top, select "Manage Content and Structure


![Manage Content and Structure](/Standards/CodeAndApplicationDesign/RulesToBeterSharePoint/PublishingImages/ManageContentAndStructure.jpg)
Figure: First step is to select 'Manage Content and Structure' to view site collection 
Once the new window opens, on the left hand side, click on the 'Clients' dropdown select New-&gt; Site. 
Note: If you don’t see this option, that means you don’t have permission to create site.

![Create New Site](/Standards/CodeAndApplicationDesign/RulesToBeterSharePoint/PublishingImages/CreateNewSiteStep1.jpg)
Figure: Create new site
Now follow these steps when the new window opens,

1. Fill in the fields for the new client site eg. Title, Description and URL
2. Select the template e.g “**ClientCollaboration\_V1**” in the Custom tab.


Note how your select is confirmed in the picture. In this example the template’s description looks like “**Site for Collaboration with SSW Clients**”.

1. Select “**Use Unique permissions**” as you need to give the client an account to visit.
2. In the “**Navigation Inheritance**” choose “**No**” as you don’t need to let client visit the other sites via the navigation.
3. Click “**Create**”


![Info to create site](/Standards/CodeAndApplicationDesign/RulesToBeterSharePoint/PublishingImages/CreateNewSiteStep2.jpg)
Figure: Fill in the appropriate info then "Create"
Next step is to setup the groups and permissions. 
Note: you can also access this through the "People and Group" option??????.

![Create new group Image](/Standards/CodeAndApplicationDesign/RulesToBeterSharePoint/PublishingImages/CreateNewSiteSetPermissionStep1.jpg)
Figure: Create a 'new group' or select an 'existing group' ?????? for the newly created site.
- Permissions: After you created the website for the client project, you need to configure the permission to make sure the developers and the clients can visit the site with the current authority.


1. On the root of the current client site, Go to Site Action - People and Groups for the client project.
2. Create a group for visitors, New - New Group.

![Create new group](/Standards/CodeAndApplicationDesign/RulesToBeterSharePoint/PublishingImages/CreateNewSiteSetPermissionStep3.jpg)
Figure: Create a 'new group' for the site?????.3. Give appropriate permissions to this group.


![Appropriate Permission](/Standards/CodeAndApplicationDesign/RulesToBeterSharePoint/PublishingImages/CreateNewSiteSetPermissionStep4.jpg)
Figure: Assign an appropriate permission to the created groups.
- Thats it all done.
- Just keep following in mind while assigning permissions.


![Group explained](/Standards/CodeAndApplicationDesign/RulesToBeterSharePoint/PublishingImages/AdditionalInfo.jpg)
Figure: Groups explained ???? REMOVE UNDERLINE
