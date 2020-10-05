---
type: rule
title: Control Choice - Do you know when to use CheckBoxes?
uri: control-choice---do-you-know-when-to-use-checkboxes
created: 2012-11-27T08:51:11.0000000Z
authors: []

---

If the option only contains 2 choices, and the answer is a Boolean type value where the opposite value is clear (e.g. Enabled/Disabled, True/False, Yes/No, On/Off), it should always be a checkbox.

[[badExample]]
| ![ Bad Example - Boolean options not using CheckBox](../../assets/NotUsingCheckBox.gif)

[[goodExample]]
| ![ Good Example - A CheckBox is used for Boolean type value   ​](../../assets/UsingCheckBox.gif)

Only 1 CheckBox is used as the opposite value is clear, such controls are often CheckBoxes in a ListView too. E.g.:

[[goodExample]]
| ![ Good Example - CheckBoxes in a ListView](../../assets/CheckBoxesInListView.gif)

CheckBoxes are also suitable to use for enable or disable sections and to tell the user that these sections do not need configuring for the application to run.

[[goodExample]]
| ![ Good Example - CheckBoxes are used ](../../assets/CheckBoxSection.gif)
(although no opposite values), because they are clear when the CheckBoxes aren't ticked, the sections are disabled
[[badExample]]
| ![ Bad Example - This screen implies that Configuring Credentials is required](../../assets/UseCheckBoxBad.gif)

[[goodExample]]
| ![ Good Example - This screen uses a CheckBox to signify that Configure Credentials is optional](../../assets/UseCheckBoxGood.gif)

If there are only two options available on the form (usually a yes/no answer), the use of a checkbox is more intuitive than radio buttons. Only use radio buttons if there are more than two options.

[[badExample]]
| ![ Bad Example – Radio buttons are not appropriate when there are only two options](../../assets/radio-for-two-options.jpg)

[[goodExample]]
| ![ Good Example – These yes/no questions have a better representation with checkboxes](../../assets/checkbox-for-two-options.jpg)
