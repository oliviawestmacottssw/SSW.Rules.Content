---
type: rule
title: Do you help the user to enter a URL field?
uri: do-you-help-the-user-to-enter-a-url-field
created: 2014-12-16T17:36:25.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

Most developers seem to validate a URL and tell the user what they have done wrong                     only after the error happens. URL fields should show how the users must enter it.
 [[badExample]]
| ![Using a validation message to tell the user to enter a correct<br>                        URL](url-field-bad.jpg)                        
The better way is to have the user avoid the error with a good default.
[[badExample]]
| ![The user has a good chance of entering the URL in the incorrect format![image showing a textfield pre-populated with 'http://www.'](url-field-good.jpg)                        ](url-field-bad2.jpg)
