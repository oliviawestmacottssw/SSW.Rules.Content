---
type: rule
title: Messages - Do you avoid giving an "Error" message for validation purposes?
uri: messages---do-you-avoid-giving-an-error-message-for-validation-purposes
created: 2012-11-27T04:26:58.0000000Z
authors: []

---

 
If you do a search and no matches are found, display a message indicating zero results were returned rather than an error message.
![](../../assets/InappropriateError.gif)Figure: Bad Example - No matches found on searching is not an "Error"   ​
However, a user thinks that either:

1. They have done something wrong (i.e. they are incompetent) OR
2. The software is broken (i.e. your application is incompetent)


Forcing the user into this opinion is a good way to make them avoid using your software in the future.

Instead, use the term "Information" when validation is required.
![Appro](../../assets/AppropriateMessage.gif)Figure: Good Example - Only use "Error" when appropriate
