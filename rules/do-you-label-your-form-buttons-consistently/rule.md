---
type: rule
title: Do you label your form buttons consistently?
uri: do-you-label-your-form-buttons-consistently
created: 2014-12-01T00:09:41.0000000Z
authors: []

---

 
​The buttons that a user will typically use to close a form should be named consistently across your applications.
 ![Broker Details - Save &amp; Close Buttons](http&#58;//www.ssw.com.au/ssw/Standards/Rules/Images/ButtonLabels_Bad.gif)Figure: Bad Example - Unclear labels on the buttons
- **Save** button could possibly update the fields but keep the form open.
- **Close** could save the fields, then close the form, when the <br>      ** Cancel** button may be more appropriate.


We recommend the age-old standards of:

- **OK**. Close the form and save any changed data. This should be referenced by the form's AcceptButton property.
- **Cancel**. Close the form without saving. This should be referenced by the form's CancelButton property.
- **Apply**. Save data without closing the form.

![Outlook Contact Properties - OK, Cancel &amp; Apply Buttons](http&#58;//www.ssw.com.au/ssw/Standards/Rules/Images/OKCancelExampleDialog.jpg)Figure: Good Example - This form uses the standard button naming standards (and has the Default buttons set!)
We have a program called     [SSW Code Auditor](http&#58;//www.ssw.com.au/ssw/CodeAuditor/) to check for this rule.

