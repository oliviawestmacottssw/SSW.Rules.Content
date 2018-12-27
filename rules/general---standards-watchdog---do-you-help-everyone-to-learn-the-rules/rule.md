---
type: rule
title: General - Standards Watchdog - Do you help everyone to learn the rules?
uri: general---standards-watchdog---do-you-help-everyone-to-learn-the-rules
created: 2009-03-10T07:08:39.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

 
"An ounce of prevention is worth a pound of cure" goes the saying. Having a strict coding standard is prevention. To create good code you must have good standards, such as commenting standards, naming standards, versioning standards and more.

**But this can really only happen if you’re going to [go the extra mile](/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=36598961-2933-4a95-ba4b-9ed702e405ef) and stick your neck out and correct someone. **
  ![mean.jpg](/PublishingImages/watchdog-mean.jpg)  Figure: Bad Example - Correcting someone in a mean way ![ghost.jpg](/PublishingImages/watchdog-ghost.jpg) Figure: Bad example - seeing a mistake and not pointing it out, doesn’t improve a person. Allow them to benefit from your experience! ![thankyou.jpg](/PublishingImages/watchdog-thankyou.jpg) Figure: Good example - say 'thank you' to a person's corrections to show you don’t have thin skin and encourage further positive and negative feedback. It all helps you to improve ![Watchdog.jpg](/PublishingImages/watchdog-watchdog.jpg) Figure: Good example - People make mistakes but correct them as though they’re a soft cute puppy 🐶
Every member of a team plays an important role in maintaining standards. Whether it's your code or someone else's, always keep an eye out for **things that can be improved**.



When you come across an error, don’t just fix it, as the developer who made it is likely to make it again. Instead, write an email to the person explaining what has been done wrong and how you would've improved the code. CC relevant parties to improve others, to [collect your brownie points](/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=27115c96-c7f0-4d6c-9500-6c7f71e67f65) or to set a good example.

No one likes being corrected but hopefully, with everyone doing this in the office, it's not a matter of finger-pointing, it is working together to write better code or developing better solutions.

### What if it’s recurring? 

When you notice someone doing the wrong thing:
- First time just send an email with a pointer to the rule
- The second time, have a very quick chat with them
- Third time call them in and give them a formal talk about it




### Going Anonymous 

If you don't have the confidence to talk to the person, send an email from info@

### Don't bottle it up 

The important thing is to talk about it at the time.

### It’s beyond code

Clearly, this standard does not just apply to write better code, it applies to all company standards. Standards are important because they ensure your experience at work is consistent and enjoyable. For example, if there was no standard to stack the dishes in the dishwasher when you were finished using them, dishes would build up and create a big mess in the kitchen!

### Be nice, not harsh 

E.g. maybe mention the word ‘tip’

### In Summary

It’s important to ensure others are doing their best to maintain and follow the standards. Remember, it can be just as important for someone’s professional development to give feedback as it is to receive it. Being able to communicate feedback in an effective and professional manner can benefit you in any career. ​

**To:** Peter
**CC:** Adam (Manager)
​
Dear Peter,

While you were away, I came across a page called ApplicationForm.aspx which was giving an error: 
'The conversion of a char data type to a DateTime data type resulted in an out-of-range DateTime value.' 
This happened when I entered '13/06/2018' into the 'Start Date' field of the form.
The error occurs because you are not using the default language of the server which is 'English' - for the users of this database FRDC. This is the same as US English format of Months first, then Days, then a four-digit Year (mm/dd/yyyy). Instead, you used 'British English' on the FRDC database which has a format of dd/mm/yyyy. Please use the standard as per Rules to Better SQLServer Databases, Rule 1200 (Middle Tier Section)

Please note that whilst inserting data from your Front End application, you should not use the format dd/mm/yyyy. Instead, you should use yyyy/mm/dd

Let's fix it together when we get to work tomorrow.

Cheers, DDK
 Figure: Good example - nicely informing of a standards violation 

