---
type: rule
archivedreason: 
title: Being Pedantic - Do your buttons have a mnemonic?
guid: 5efb94c3-e91f-4a8c-87ba-b1bc76edf533
uri: being-pedantic-do-your-buttons-have-a-mnemonic
created: 2012-11-27T09:25:36.0000000Z
authors:
- id: 1
  title: Adam Cogan
related: []
redirects: []

---

A mnemonic for a button is the letter which has an underscore, and the user can press the button using Alt-<char>.</char>

<!--endintro-->

[[badExample]]
| ![All buttons without Mnemonic](../../assets/BadMem.gif)
[[goodExample]]
| ![All buttons with Mnemonic - user can easily choose which button they want without a click](../../assets/GoodMem.gif)
In Windows Applications, it is quite easy to assign a mnemonic to a button with the "&" character.

So for the case above, the text would be:

btnAbout.Text = "&About"

 **Tip:** In Windows XP the mnemonic display effects can be hidden by Default and then shown every time the user presses the Alt key.
