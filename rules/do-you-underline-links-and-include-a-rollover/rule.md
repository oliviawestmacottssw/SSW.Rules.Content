---
type: rule
title: Do you underline links (and include a rollover)?
uri: do-you-underline-links-and-include-a-rollover
created: 2015-02-16T01:30:13.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 44
  title: Duncan Hunter
- id: 16
  title: Tiago Araujo

---

Always make links perfectly clear.
 
It's very important that your links stand out from the background as well as the surrounding text. A solid underline and a contrasting color is the usually the best choice, but the exact method is not important as long as the end result stands out. A link should not only be discoverable upon accidental hovering.

Rollovers are important as they offer visual feedback to a user that this link that will take them somewhere. While there is a myriad of ways to do this; you can't go wrong with an underline or border-bottom.

[greyBox]
 For more information on this, please [go to SSW website](https://www.ssw.com.au/).
 
[/greyBox]
Bad Example: The link is hard to recognize

[greyBox]
 For more information on this, please [go to SSW website](https://www.ssw.com.au/). 
 
[/greyBox]
Good Example: This link is obvious



![Obvious rollover. You can test it by hovering the links on the example above](link-hover.jpg)

Example CSS for rollover:

a:hover { 
    color: #cc4141;
    cursor: pointer;
}
Figure: Example CSS for rollover effect
