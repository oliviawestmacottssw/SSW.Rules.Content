---
type: rule
title: Do you group related fields by using FieldSet?
uri: do-you-group-related-fields-by-using-fieldset
created: 2014-12-22T11:52:59.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

**FieldSet** element allows you to group thematically related controls                     and labels. Grouping controls makes forms more accessible and easier for users to                     understand the purpose of filling the forms.

See the example below using "Your Details"                     and "Event Details".
 
[[goodExample]]
| ![Use FieldSet for grouping](fieldset.jpg)
Here's an example of how FieldSet works:


```
Your Details
    
        First Name: 
        
        Last Name: 
        
        Email Address:
```

Figure: Example code of FieldSet <br>   
![How that code will look on the browser](fieldset-browser.jpg)
 Things to remember:

1. Wrap logical control groups in a .
2. The first child of a  should be a , so the user knows what to expect in that section.
