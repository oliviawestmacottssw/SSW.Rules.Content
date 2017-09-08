---
type: rule
title: Do you know how to send newsletter in Microsoft CRM 2013?
uri: do-you-know-how-to-send-newsletter-in-microsoft-crm-2013
created: 2013-03-13T14:14:13.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 4
  title: Ulysses Maclaren

---

 
​​​Email newsletters can be sent and responses can be tracked using Microsoft Dynamic CRM 2013:
 
There is more than one way to distribute a newsletter through CRM, such as through Campaigns and Quick Campaigns. The way detailed below is the simplest method, using Quick Campaigns.

1. Find contacts that you will send the newsletters to. <br>      
The first time - use <br>      **Advanced Find** in CRM 2013, then save it as a System View. In the example below, we're only interested in New Zealand contacts.
Subsequent times - Use the **System View**, so everyone is using the same list.
![crm01.png](/PublishingImages/crm01.png)Figure: From the CRM home screen, hover your mouse over “Workplace”, and then click “Contacts” in the menu that drops down![crm02.png](/PublishingImages/crm02.png)Figure: From the “Activities” page, click “…” | “Advanced Find”. This will activate a pop-up.![crm03.png](/PublishingImages/crm03.png)Figure: Select Contacts at Look For and specify a set of criteria to search for newsletter contacts
![crm04 - results.png](/PublishingImages/crm04%20-%20results.png)Figure: then select "Results" to bring up contacts which match your search query![crm05 - contacts list.png](/PublishingImages/crm05%20-%20contacts%20list.png)Figure: The result contacts that will get newsletter: these contacts allow us to "Send Marketing Material" and have a New Zealand email address or living country is New Zealand
2. ​First time only, save this as a System View. You will need a SysAdmin for this.
3. Create the newsletter in Microsoft CRM 2013 using a <br>            **Quick Campaign**![Create Quick Campaign](/PublishingImages/crm06%20-%20create%20quick%20campaign.png)Figure: Select "For All Records on All Pages" to create a Quick Campaign from the current contact list. This will bring up a Quick Campaign Wizard
![Specify name of quick campaign](/PublishingImages/crm07%20-%20name%20quick%20campaign.png)Figure: Click Next and then specify the name of the quick campaign.![Select the Activity Type and Owner](/PublishingImages/crm08-%20own%20quick%20campaign.png)Figure: Select the Activity Type and Owner.![Fill in newsletter Content](/PublishingImages/crm09%20-%20add%20content.png)Figure: Fill in newsletter content.    **Attention: SSW Employees**
You need to follow the instructions in SSW Standards Internal for preparing the newsletter. It's a manual checklist so you don't make any mistakes.
​    Use your preferred browser to view the content of the newsletter, select all (or use "Ctrl" + "A") and then copy and paste it in the Quick Campaign text area.
![Newsletter Ubsubscribe](/PublishingImages/crm10%20-%20unsubscribe.png)Figure: Highlight the keyword and click the Unsubscribe button to make a link for subscribers to unsubscribe themselves.4. Click <br>            **Next** to create all email activities in Microsoft CRM 2013.
5. Now you have to wait while the emails send out:
    - **Bad Example - Microsoft CRM Outlook** for outgoing email, then you need to open your Microsoft Outlook, so the email activities can be promoted to Outlook and sent out. This method is slow because of the synchronization process between CRM and Microsoft Outlook and you need to leave outlook open during the entire process.
    - **Good Example - Email router** for outgoing email, then those email activities will be sent out automatically by Email router. This method is our preferred method of sending the newsletter, CRM email router can be configured to send out newsletters immediately and the user doesn't have to open Outlook while the emails are being processed.


