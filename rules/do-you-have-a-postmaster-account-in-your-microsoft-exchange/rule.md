---
type: rule
title: Do you have a postmaster account in your Microsoft Exchange?
uri: do-you-have-a-postmaster-account-in-your-microsoft-exchange
created: 2015-04-10T18:59:46.0000000Z
authors:
- id: 47
  title: Stanley Sidik

---

 
### ​What is a postmaster account? 

It is an RFC mandated specification email address use to identify the administrator of a mail server. Any errors in email processing are directed to the postmaster address.

The email received at this address is sent to the mail server administrator, in our case the SysAdmins.
 
At SSW we have configured     [postmaster@ssw.com.au](mailto&#58;postmaster@ssw.com.au) as a distribution group, with mail server administrators as members of this distribution group.
![postmaster.png](/PublishingImages/postmaster.png)Figure: Group members of postmaster@ssw.com.au​
