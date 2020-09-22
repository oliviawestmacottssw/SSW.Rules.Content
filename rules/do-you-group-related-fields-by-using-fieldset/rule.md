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
 <dl class="goodImage"><dt> 
      <img src="fieldset.jpg" alt=""> 
   </dt><dd>Figure: Good example - Use FieldSet for grouping</dd><dd></dd></dl>
Here's an example of how FieldSet works:
<dl class="code"><dt><pre><fieldset>
    <legend>Your Details</legend>
    <p>
        <label for="FirstName">First Name: </label>
        <input id="FirstName" type="text"><br>
        <label for="LastName">Last Name: </label>
        <input id="LastName" type="text"><br>
        <label for="EmailAddress">Email Address: </label>
        <input id="EmailAddress" type="text">
    </p>
</fieldset></pre></dt><dd>Figure: Example code of FieldSet</dd></dl><dl class="image">​ 
   <dt> 
      <img src="fieldset-browser.jpg" alt=""> 
   </dt><dd>Figure: How that code will look on the browser</dd><dd></dd></dl>
​ Things to remember:

1. Wrap logical control groups in a <fieldset>.</fieldset>
2. The first child of a <fieldset> should be a <legend>, so the user knows what to expect in that section.</legend></fieldset>

​  
