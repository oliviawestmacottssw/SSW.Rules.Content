---
type: rule
title: Forms - Do you indicate which fields are required and validate them?
uri: forms---do-you-indicate-which-fields-are-required-and-validate-them
created: 2014-12-04T19:32:54.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

Always indicate which fields are required. Users get frustrated when they experience a wasted trip to the server, just because they did not get an obvious indication of what was required first time around.
 
[[badExample]]
| ![No visual indication for required fields when a user first sees the form](Required-field_Bad-example.jpg)
A designer will know the best way to indicate required field depending on the layout. However if you are in doubt and don’t have a designer around, a red asterisk is definitely the best option.

[[goodExample]]
| ![A visual indication of what fields are required](Redstar_Good-example.jpg)(use a red asterisk if you are not a designer)
#### More Information

You should combine these visual indicators with appropriate client and server side validators to make sure that your data conforms to business requirements. Adding a RequiredFieldValidator to the above textboxes gives you data validity check with minimal coding.


Figure: Bad Example - No validator used, so the user won't know the email is required
ID="emailReqValidator" />
Figure: Good Example - an ASP.NET validator in use, to indicate the fields required
[[greyBox]]
|  
| **Note:** For ASP.NET Dynamic Data although validation is done differently (under the covers it is using a field template + the ASP.NET validator).
|
