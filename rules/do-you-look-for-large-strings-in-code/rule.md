---
type: rule
title: Do you look for large strings in code?
uri: do-you-look-for-large-strings-in-code
created: 2012-04-01T09:17:55.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 23
  title: Damian Brady

---

Long hard-coded strings in a codebase can be a sign of poor architecture.
 
To make hard-coded strings easier to find, [consider highlighting them in your IDE](/do-you-highlight-strings-in-your-code-editor).

[[badExample]]
| ![ Bad Example - The connection string is hard-coded and isn't easy to see in the IDE.](LongStringBadExample.png)

![ Better Example - The connection string is still hard-coded, but at least it's very visible to the developers.](longstringbadexample2.png)

[[goodExample]]
| ![ Good Example - The connection string is now stored in configuration and we don't have a long hard-coded string in the code.](ShortStrings.png)
