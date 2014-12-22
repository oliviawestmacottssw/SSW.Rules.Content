---
type: rule
title: Do you group related fields by using FieldSet?
uri: do-you-group-related-fields-by-using-fieldset
created: 2014-12-22T11:52:59.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

 
**​FieldSet** element allows you to group thematically related controls                     and labels. Grouping controls makes forms more accessible and easier for users to                     understand the purpose of filling the forms.

See the example below using "Your Details"                     and "Event Details".
 ![](/PublishingImages/fieldset.jpg)Figure: Good example - Use FieldSet for grouping
Here's an example of how FieldSet works:


```
<fieldset>
    <legend>Your Details</legend>
    <p>
        <label for="FirstName">First Name: </label>
        <input id="FirstName" type="text" /><br />
        <label for="LastName">Last Name: </label>
        <input id="LastName" type="text" /><br />
        <label for="EmailAddress">Email Address: </label>
        <input id="EmailAddress" type="text" />
    </p>
</fieldset>
```

Figure: Example code of FieldSet​ <br>   ![](/PublishingImages/fieldset-browser.jpg)Figure: How that code will look on the browser
​ Things to remember:

1. Wrap logical control groups in a &lt;fieldset&gt;.
2. The first child of a &lt;fieldset&gt; should be a &lt;legend&gt;, so the user knows what to expect in that section.

​  
