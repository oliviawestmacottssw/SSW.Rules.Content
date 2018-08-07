---
type: rule
title: General - Standards Watchdog - Do you help everyone to learn the rules?
uri: general---standards-watchdog---do-you-help-everyone-to-learn-the-rules
created: 2009-03-10T07:08:39.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

 ​​​​​​"An ounce of prevention is worth a pound of cure" goes the saying. Having a strict coding standard is prevention. To create good code you must have good standards, such as commenting standards, naming standards, versioning standards and more. <br>
  ![Watchdog.jpg](/PublishingImages/fb339f_Watchdog.jpg)  Figure: Be a fearsome Standards Watchdog
Every member of a team plays an important role in maintaining standards. Whether it's my code or someone else's, I always keep an eye out for mistakes.

When I come across an error, I never just fix it, as the developer who made it is likely to make it again. I write an email to the person explaining what has been done wrong and how to do the right thing. I CC the manager so they are aware of the situation.

Of course, with everyone doing this in the office, it's not a matter of finger pointing, we all truly work together to write better code.
When you notice someone doing the wrong thing
- First time just send an email with a pointer to the rule
- Second time, have a very quick chat with them
- Third time call them in and give them a formal talk about it


If you don't have the confidence to talk to the person, send an email from info. The important thing is to talk about it at the time.

Clearly, this standard does not just apply to writing better code, it applies to **all company standards**. Standards are important because they ensure your experience at work is consistent and enjoyable. For example, if there was no standard to stack the dishes in the dishwasher when you were finished using them, dishes would build up and create a big mess in the kitchen!

Equally important is your responsibility to ensure that others are doing their best to maintain and follow the standards.

**To:** Peter
**CC:** Adam (Manager)
​
Dear Peter,

While you were away, I came across a page called ApplicationForm.aspx which was giving an error: 
'The conversion of a char data type to a datetime data type resulted in an out-of-range datetime value.' 
This happened when I entered '13/06/2002' into a the 'Start Date' field of the form.
The error occurs because you are not using the default language of the server which is 'English' - for the users of this database FRDC. This is the same as US English format of Months first, then Days, then a four digit Year (mm/dd/yyyy). Instead, you used 'British English' on the FRDC database which has a format of dd/mm/yyyy. Please use the standard as per Rules to Better SQLServer Databases, Rule 1200 (Middle Tier Section)
Please note that whilst inserting data from your Front End application, you should not use the format dd/mm/yyyy. Instead you should use yyyy/mm/dd

Let's fix it together when we get to work tomorrow.

Cheers, DDK
 
 Figure: Make sure you let your client know if you find a standards violation
