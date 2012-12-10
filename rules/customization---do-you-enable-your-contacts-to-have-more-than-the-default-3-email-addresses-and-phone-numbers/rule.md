---
type: rule
title: Customization - Do you enable your contacts to have more than the default 3 email addresses and phone numbers?
uri: customization---do-you-enable-your-contacts-to-have-more-than-the-default-3-email-addresses-and-phone-numbers
created: 2012-12-10T20:02:07.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

 Out of the box CRM4 only enables a contact to have 3 phone numbers (home, business and mobile) + 3 email addresses (but only one visible). A customization that almost everyone needs is to remove this limitation (to allow contacts to have an unlimited amount of phone numbers and email addresses). ![](/SoftwareDevelopment/RulesToBetterCRMForDevelopers/PublishingImages/contact1.jpg)**Figure: Bad example - Out of the box a contact can only have 3 phone numbers and<br>              1 email address **
There are a few customizations needed to get the SSW Contact Makeover:

- Show some hidden fields
- Make some form changes to move to a new tab
- Make a CRM frame (to add in a subform)
- Add some entities
- Add some form java script to hide the core Contact Details? tab when a user is<br>            entering a new contact

![](/SoftwareDevelopment/RulesToBetterCRMForDevelopers/PublishingImages/contact3.jpg)**Figure: Good example - Enable the hidden fields and move it to a new tab. And now<br>              a Contact has 3 email addresses and phone numbers **![](/SoftwareDevelopment/RulesToBetterCRMForDevelopers/PublishingImages/contact2.jpg)**Figure: Good example - After adding an entity, you add a frame show the unlimited<br>              contact details (phone, fax, email etc) **
Q: So what is the end result? 
A: The end user experience to add a phone number is ..
![](/SoftwareDevelopment/RulesToBetterCRMForDevelopers/PublishingImages/contact4.jpg)**Figure:  Step 1: Double-click the contact (or right-click the contact and<br>              select Open) Open**
![](/SoftwareDevelopment/RulesToBetterCRMForDevelopers/PublishingImages/contact5.jpg)**Figure:  Step 2: Select the tab 'More Contact Details' **
![](/SoftwareDevelopment/RulesToBetterCRMForDevelopers/PublishingImages/contact6.jpg)**Figure:  Step 3: Click the button 'New Contact Detail' **
![](/SoftwareDevelopment/RulesToBetterCRMForDevelopers/PublishingImages/contact7.jpg)**Figure:  Step 4: Enter the details and click button 'Save and Close' (top<br>              left) **
