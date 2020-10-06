---
type: rule
title: Do you give users least privileges?
uri: do-you-give-users-least-privileges
created: 2018-04-09T21:28:47.0000000Z
authors:
- id: 71
  title: Steven Andrews

---

Like other services, it is important that your company has a structured and secure approach to managing Azure Permissions.

First a little understanding of how Azure permissions work. For each subscription, there is an Access Control (IAM) section that will allow you to grant overall permissions to this Azure subscription. It is important to remember that any access that is given under Subscriptions | "Subscription Name" | Access Control (IAM), will apply to all Resource Groups within the Subscription.
 
[[badExample]]
| ![too many people have Owner permission on the subscription level](azure-permissions-bad.jpg)
[[goodExample]]
| ![only Administrators that will be managing overall permissions and content have been given Owner/Co-administrator](azure-permissions-good.png)
From the above image, only the main Administrators have been given Owner/Co-administrator access, all other users within the SSWDesigners and ** SSWDevelopers** Security Groups have been given Reader access. The **SSWSysAdmins** Security group has also been included as an owner which will assist in case permissions are accidentally stripped from the current Owners.
