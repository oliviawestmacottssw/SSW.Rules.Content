---
type: rule
title: Customization - Do you enable your contacts to have more than the default 3 email addresses and phone numbers?
uri: customization---do-you-enable-your-contacts-to-have-more-than-the-default-3-email-addresses-and-phone-numbers
created: 2012-12-10T20:02:07.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

Out of the box CRM4 only enables a contact to have 3 phone numbers (home, business and mobile) + 3 email addresses (but only one visible). A customization that almost everyone needs is to remove this limitation (to allow contacts to have an unlimited amount of phone numbers and email addresses). ![ Bad example - Out of the box a contact can only have 3 phone numbers and<br>              1 email address](contact1.jpg)
There are a few customizations needed to get the SSW Contact Makeover:

- Show some hidden fields
- Make some form changes to move to a new tab
- Make a CRM frame (to add in a subform)
- Add some entities
- Add some form java script to hide the core Contact Details? tab when a user is<br>            entering a new contact

![ Good example - Enable the hidden fields and move it to a new tab. And now<br>              a Contact has 3 email addresses and phone numbers ![](contact2.jpg)](contact3.jpg)
Q: So what is the end result? 
A: The end user experience to add a phone number is ..
![  Step 1: Double-click the contact (or right-click the contact and<br>              select Open) Open![](contact5.jpg)](contact4.jpg)
![  Step 3: Click the button 'New Contact Detail' ![](contact7.jpg)](contact6.jpg)
