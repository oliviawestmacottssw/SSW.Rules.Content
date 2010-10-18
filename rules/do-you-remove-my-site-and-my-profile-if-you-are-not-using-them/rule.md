---
type: rule
title: Do you remove ‘My Site’ and ‘My Profile’ if you are not using them?
uri: do-you-remove-my-site-and-my-profile-if-you-are-not-using-them
created: 2010-10-15T08:33:09.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 8
  title: John Liu
- id: 9
  title: William Yin

---


**My Site** and **My Profile** are great but if you are not using them, it makes sense to remove them:
![](/Standards/SoftwareDevelopment/RulesToBetterSharePoint/PublishingImages/LinksNeedToBeRemove.png) Figure: Links need to be hidden

You can follow below steps to hide “My Site” and “My Profile”,
<br>There are a few options, based on what you need to do:


- **Delete the association** (not recommended)<br>    

> a. Go to **Central Admin**     | **Application Management** | **Service Applications**     | **Configure service application associations**, 
>      Choose “default” link:     
> ![](/Standards/SoftwareDevelopment/RulesToBetterSharePoint/PublishingImages/RemoveAssociation.png)Figure: Choose “default” link
> 
> b.Uncheck the “**User Profile Service Application**”  in the     opened page, then click “**OK**”:![](/Standards/SoftwareDevelopment/RulesToBetterSharePoint/PublishingImages/RemoveAssociation2.png)
> Figure: uncheck the association for user<br>    profile service
- **Customize permissions for only some people to have access to create personal site**

> You can remove it for most people - but leave it for only some users.
> 
> a.   <br>    Go to **Central Admin** | **Application Management**<br>    | **Service Applications** | **Manage service applications**,
> <br>    Click the link of “User Profile Service Application”, navigate to its manage<br>    page:**![](/Standards/SoftwareDevelopment/RulesToBetterSharePoint/PublishingImages/UserProfileServiceManagePage.png)
> **Figure: “User Profile<br>    Service Application” manage page
> 
> b.    Click     **People** | **Manage User Permissions**, you can     customize the user profile permission for specific users:**![](/Standards/SoftwareDevelopment/RulesToBetterSharePoint/PublishingImages/CustomUserProfileServicePermission.png)
> **Figure: Better - customize User profile<br>    permission
- **Delete the service** (recommended if you don't need the service at all in your farm)<br>    

> **Note**: You can always create it later if you need it in the     future.
> 
>      Go to **Central Admin** | **Application Management** |     **Service Applications** | **Manage service applications**,
> 
> Select “User Profile Service Application”, then click the<br>    “Delete” button on the ribbon:**![](/Standards/SoftwareDevelopment/RulesToBetterSharePoint/PublishingImages/DeleteUserProfileService.png)
> **Figure: Best - delete user profile<br>    service


**Note**:<br>    Later on if you want to get My Site working read these 2 links… unless Microsoft<br>    creates a services that fixes User Profile Synchronization service…. thanks to<br>    Mark Rhodes for these tips…
[http://www.harbar.net/articles/sp2010ups2.aspx](http&#58;//www.harbar.net/articles/sp2010ups2.aspx)    and [http://www.harbar.net/articles/sp2010ups.aspx](http&#58;//www.harbar.net/articles/sp2010ups.aspx)




