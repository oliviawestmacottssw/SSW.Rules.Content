---
type: rule
title: Do you use the security options in Outlook?
uri: do-you-use-the-security-options-in-outlook
created: 2009-04-03T08:20:20.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 2
  title: Cameron Shaw

---

 
When you distribute important information by email all you can do is put "Do Not Forward this please". Important corporate information should be protected better than this.
![Outlook 2003 IRM Do Not Forward](/Communication/RulesToBetterEmail/PublishingImages/outlookIRM.jpg)Figure: With Outlook 2010 IRM you can protect your email messages 
A solution exists in Microsoft Office 2010 which you will see built into Outlook 2010 (and the rest of Office [except Access]), entitled 'Information Rights Management', a file level security application built onto Windows Server 2010. The capability enables you to prevent recipients of your emails (and attachments) from forwarding them on, copying any text, or printing the document (be aware that determined chaps could use a lower level screen shot program to get past this). Additionally, it encrypts the file as it's sent away. As an added basis - you can secure on a group level (based on Active Directory groups). To prevent an email being forwarded simply create a new email and select the "options" tab and click on "permission" in the ribbon and select "do not forward".
![Outlook 2003 IRM Do Not Forward](/Communication/RulesToBetterEmail/PublishingImages/outlook-prevent-FW.jpg)Figure: How to prevent emails being forwarded in Outlook 2010
If you're not running Office 2010 install the [IRM for Internet Explorer download](http&#58;//www.ssw.com.au/ssw/Redirect/Microsoft/Office2003IRMDownload.htm).

BTW you may be interested to know that every mail item that you send gets a file saved with these credentials so you can still open the emails when you are offline. To see: go to Start - Run %USERPROFILE%\Local Settings\Application Data\Microsoft\drm.

