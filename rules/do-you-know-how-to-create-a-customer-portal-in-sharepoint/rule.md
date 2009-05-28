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

 
You always need to collaborate with your customer.  They want to see new mockups, comment on features, get new releases and participate in team discussions on their particular project.

So the first thing you should do is to create a customer portal in your SharePoint extranet, and give your customer a login so they can jump in and get involved!

We use a customized SharePoint Team Collaboration site template to quickly initialize a new site for our customers.

Do you know how to create a customer portal?
 
Follow the following steps to create a Client Site.

- Go to the root where you want to create a site, i.e sharepoint.ssw.com.au
- Click "Site Actions" on right hand top, select "Manage Content and Structure


![Manage Content and Structure](/Standards/CodeAndApplicationDesign/RulesToBeterSharePoint/PublishingImages/ManageContentAndStructure.jpg)
Figure: Manage Content and Structure to view site collection 
- New window will open, on the left hand side, click on the dropdown of the clients and select New-&gt;Site. NOTE: If you don’t see this option, that means you don’t have permission to create site, talk to John or Joe to grant you appropriate permission.


![Create New Site](/Standards/CodeAndApplicationDesign/RulesToBeterSharePoint/PublishingImages/CreateNewSiteStep1.jpg)
Figure: Create new site
- Now follow these steps when the new window opens,


1. Fill in the new client project website’s Title, Description and URL name.
2. Select a template called “**ClientCollaboration\_V1**” in the Custom tab.
3. Check the template’s description looks like “**Site for Collaboration with SSW Clients**”.
4. Select “**Use Unique permissions**” for this new site in “**Permissions**” as you need to give the client an account to visit this client project website “**only”**.
5. Choice “**No**” in the “**Navigation Inheritance**” part as you don’t need to let client visit the other sites via the navigation.
6. Click “Create” to create the new website for the client project.


![Info to create site](/Standards/CodeAndApplicationDesign/RulesToBeterSharePoint/PublishingImages/CreateNewSiteStep2.jpg)
Figure: Fill in the appropriate info to created site.
- You can setup groups and permission here, or through the "People and Group" as shown in next step.


![Create new group Image](/Standards/CodeAndApplicationDesign/RulesToBeterSharePoint/PublishingImages/CreateNewSiteSetPermissionStep1.jpg)
Figure: Create a new group or select an existing group for the newly created site.
- Permissions: After you created the website for the client project, you need to configure the permission to make sure the developers and the clients can visit the site with the current authority.


1. On the root of the current client site, Go to Site Action - People and Groups for the client project.
2. Create a group for visitors, New - New Group.

![Create new group](/Standards/CodeAndApplicationDesign/RulesToBeterSharePoint/PublishingImages/CreateNewSiteSetPermissionStep3.jpg)
Figure: Create a new group for the site.3. Give appropriate permission to this group.


![Appropriate Permission](/Standards/CodeAndApplicationDesign/RulesToBeterSharePoint/PublishingImages/CreateNewSiteSetPermissionStep4.jpg)
Figure: Assign an appropriate permission to the created groups.
- Thats it all done.
- Just keep following in mind while assigning permissions.


![Group explained](/Standards/CodeAndApplicationDesign/RulesToBeterSharePoint/PublishingImages/AdditionalInfo.jpg)
Figure: Groups explained.
