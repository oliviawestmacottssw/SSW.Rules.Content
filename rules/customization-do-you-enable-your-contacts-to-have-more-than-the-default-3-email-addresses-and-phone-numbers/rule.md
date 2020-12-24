---
type: rule
archivedreason: 
title: Customization - Do you enable your contacts to have more than the default 3 email addresses and phone numbers?
guid: 8f91c1c2-5746-4142-b46a-11ef7d2d322b
uri: customization-do-you-enable-your-contacts-to-have-more-than-the-default-3-email-addresses-and-phone-numbers
created: 2012-12-10T20:02:07.0000000Z
authors:
- id: 1
  title: Adam Cogan
related: []
redirects: []

---

Out of the box CRM4 only enables a contact to have 3 phone numbers (home, business and mobile) + 3 email addresses (but only one visible). A customization that almost everyone needs is to remove this limitation (to allow contacts to have an unlimited amount of phone numbers and email addresses). 
<!--endintro-->

[[badExample]]
| ![Out of the box a contact can only have 3 phone numbers and               1 email address](contact1.jpg)
There are a few customizations needed to get the SSW Contact Makeover:

* Show some hidden fields
* Make some form changes to move to a new tab
* Make a CRM frame (to add in a subform)
* Add some entities
* Add some form java script to hide the core Contact Details? tab when a user is<br>            entering a new contact


[[goodExample]]
| ![Enable the hidden fields and move it to a new tab. And now               a Contact has 3 email addresses and phone numbers](contact3.jpg)
[[goodExample]]
| ![After adding an entity, you add a frame show the unlimited               contact details](contact2.jpg)(phone, fax, email etc)         
Q: So what is the end result? 
A: The end user experience to add a phone number is ..

![Step 1: Double-click the contact](contact4.jpg)(or right-click the contact and               select Open) Open          
![Step 2: Select the tab 'More Contact Details'](contact5.jpg)

![Step 3: Click the button 'New Contact Detail'](contact6.jpg)
![Step 4: Enter the details and click button 'Save and Close'](contact7.jpg)(top               left)
