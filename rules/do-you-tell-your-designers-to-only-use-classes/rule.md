---
type: rule
title: Do you tell your designers to only use classes?
uri: do-you-tell-your-designers-to-only-use-classes
created: 2013-04-10T21:08:06.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

In Sitefinity you can alter the appearance and content areas on your webpage using "Layouts". These layouts are basically just Divs with sizes applied.
 
![You have the ability to assign a Class to a Div only. No other customisations can be made](sitefinity-class-only.jpg)
Additionally, Sitefinity will hard code the widths of the layout and there is no way to stop it.
 The hack work around is to manually remove the widths via JQuery:


[[greyBox]]
|  
| $(".sf\_colsOut").css("width", "");
|
