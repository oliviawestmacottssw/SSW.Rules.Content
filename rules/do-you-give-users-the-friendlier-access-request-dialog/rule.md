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

​Instead of displaying a direct "**Access Denied**" warning info, you can allow end users to send an "**Access Request**".

![ Joanna is requesting access to SharePoint site](PermissionRequest.jpg)

 
​The "request manager" will receive an email:

![ Request Notification Email SampleThe link in the email will navigate administrator to the Pending Requests list:](637cf8_RequestNotificationEmail.png)

![ Pending Requests List](LinkToPendingRequestsList.png)

After reading the request infomation, the administrator can "Approve" or "Decline" the request, o​r he can start a conversation with the request user on the **Pending Requests** list directly to inquire more information:

![ possible actions for requests ](StartAConversatioinOnPendingList.png)
(Approve, Decline or start a conversation with the request user)


To setup permission request for a SharePoint site collection, go to "**Site Settings (Gear Wheel icon)** | **Site Permissions**":

![ Open "Access Request" setting](SetupPermissionRequest.png)



**​​​​Limition:**
This "Access Request" only works for authenticated users to inquire more access permission, that means if your site allows "anonymous access", then an anonymous user cannot send "access request" as he doesn't have an identify to be assigned more access permission​.
