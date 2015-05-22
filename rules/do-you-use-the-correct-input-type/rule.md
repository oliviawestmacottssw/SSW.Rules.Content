---
type: rule
title: Do you use the correct input type?
uri: do-you-use-the-correct-input-type
created: 2015-05-22T03:02:36.0000000Z
authors: []

---

 
HTML5 introduced a whole slew of new type properties for forms. Gone are the days of just using type="text" for every field in a form (barring buttons and checkboxes).

Although most of these don't do anything on desktop, on mobile devices they bring up the correct keyboard. As we move into a more mobile digital age, small things like the proper numerical keyboard or a keyboard with a quick ".com" becomes increasingly important.
 
![](/PublishingImages/fieldtype-text.PNG)

&lt;label for="phone"&gt;Phone&lt;/label&gt;: &lt;input           type="text" name="phone"&gt;&lt;/input&gt;
Figure: Bad Example – This field is using a text type and shows a standard keyboard on mobile

![](/PublishingImages/fieldtype-tel.PNG)

&lt;label for="phone"&gt;Phone&lt;/label&gt;: &lt;input           type="tel" name="phone"&gt;&lt;/input&gt;
Figure: Good Example – This field is using the correct field type and shows the keypad on mobile


Here is a table of some useful input types and what they do:


| Type | What |
| --- | --- |
| Color | This is a color picker. This is not supported on mobile or in all browsers. |
| Date | This brings up the date picker on mobile |
| Datetime-local | This brings up a date-time picker on mobile |
| Email | This adds ".com" and "@" to the keyboard on mobile |
| File | Use then when you want a button to upload files. This will also allow users to upload from their mobile device’s photo library. |
| Month | This brings up a month and year picker on mobile |
| Number | This displays as a number selector on desktop and can be set with upper and lower limits. However, it does not work on mobile yet. |
| Password | This masks the characters and should be used for any privacy sensitive information |
| Range | This will show a slider control and works on mobile |
| Search | This should be used to define search fields |
| Tel | This brings up the number pad on mobile |
| Time | This brings up the time picker on mobile |
| URL | This adds ".com" to the keyboard on mobile |


