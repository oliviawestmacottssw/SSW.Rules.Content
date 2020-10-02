---
type: rule
title: Messages - Do you know how to put the technical info? (2/3 Description)
uri: messages---do-you-know-how-to-put-the-technical-info-23-description
created: 2012-11-27T04:36:22.0000000Z
authors: []

---

#### Description

The description should explain *what the error was*, followed by the *why it occurred*. Information that is useful for debugging should be included with errors where possible in a "Details" section. You should also avoid making the text unnecessarily wide. e.g.
 
[[badExample]]
| ![ Bad Example - A message box that does not intuitively alert the user](../../assets/BadMessageBox.gif)

- This is confusing, because it uses different terminology to the title ("estimate" instead of "quote")
- There is no punctuation
- The word "Error" is meaningless
- Line breaks are not present, so the message box is too wide and the text may wrap in the wrong spot


[[goodExample]]
| ![ Good Example - A message box that is clear, consistent and intuitive](../../assets/GoodMessageBox.gif)

- Terminology is consistent
- Punctuation is present
- "Details" indicates that this information is useful for debugging
- The text is split across three lines, and the technical information after Details is separated from the description of the error
