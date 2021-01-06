---
type: rule
archivedreason: 
title: Do you group related fields by using FieldSet?
guid: 733a5e44-94b1-4226-99c6-ba94b27d0eb4
uri: do-you-group-related-fields-by-using-fieldset
created: 2014-12-22T11:52:59.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
related: []
redirects: []

---

**FieldSet** element allows you to group thematically related controls                     and labels. Grouping controls makes forms more accessible and easier for users to                     understand the purpose of filling the forms.

See the example below using "Your Details"                     and "Event Details".

<!--endintro-->
<dl class="goodImage"><dt> 
      <img src="fieldset.jpg" alt=""> 
   </dt><dd>Figure: Good example - Use FieldSet for grouping</dd><dd></dd></dl>
Here's an example of how FieldSet works:
<dl class="code"><dt><pre>&lt;fieldset&gt;
    <legend>Your Details</legend>
    <p>
        <label for="FirstName">First Name: &lt;/label&gt;
        <input id="FirstName" type="text"><br>
        <label for="LastName">Last Name: &lt;/label&gt;
        <input id="LastName" type="text"><br>
        <label for="EmailAddress">Email Address: &lt;/label&gt;
        <input id="EmailAddress" type="text">
    </label></label></label></p>
&lt;/fieldset&gt;</pre></dt><dd>Figure: Example code of FieldSet</dd></dl><dl class="image"> 
   <dt> 
      <img src="fieldset-browser.jpg" alt=""> 
   </dt><dd>Figure: How that code will look on the browser</dd><dd></dd></dl>
Things to remember:

1. Wrap logical control groups in a &lt;fieldset&gt;.
2. The first child of a &lt;fieldset&gt; should be a <legend>, so the user knows what to expect in that section.</legend>
