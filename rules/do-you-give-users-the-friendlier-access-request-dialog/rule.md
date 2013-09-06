---
type: rule
title: Do you give users the friendlier Access Request dialog?
uri: do-you-give-users-the-friendlier-access-request-dialog
created: 2013-07-16T02:20:38.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 9
  title: William Yin

---

 Instead of displaying a direct "**Access Denied**" warning info, you can allow end users to send an "**Access Request**".
![PermissionRequest.jpg](/PublishingImages/PermissionRequest.jpg)Figure: Joanna is requesting access to SharePoint site
 
​The "request manager" will receive an email:
![RequestNotificationEmail.png](/PublishingImages/637cf8_RequestNotificationEmail.png)Figure: Request Notification Email SampleThe link in the email will navigate administrator to the **Pending Requests** list:![LinkToPendingRequestsList.png](/PublishingImages/LinkToPendingRequestsList.png)Figure: Pending Requests List
After reading the request infomation, the administrator can "Approve" or "Decline" the request, o​r he can start a conversation with the request user on the **Pending Requests** list directly to inquire more information:
![StartAConversatioinOnPendingList.png](/PublishingImages/StartAConversatioinOnPendingList.png)Figure: possible actions for requests (Approve, Decline or start a conversation with the request user)


To setup permission request for a SharePoint site collection, go to "**Site Settings (Gear Wheel icon)** | **Site Permissions**":
![SetupPermissionRequest.png](/PublishingImages/SetupPermissionRequest.png)Figure: Open "Access Request" setting


**​​​​Limition:**
This "Access Request" only works for authenticated users to inquire more access permission, that means if your site allows "anonymous access", then an anonymous user cannot send "access request" as he doesn't have an identify to be assigned more access permission​.



