---
type: rule
archivedreason: 
title: Do you underline links (and include a rollover)?
guid: aaef4269-0a29-4752-b3eb-a6920b9bd373
uri: do-you-underline-links-and-include-a-rollover
created: 2015-02-16T01:30:13.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
- title: Duncan Hunter
  url: https://ssw.com.au/people/duncan-hunter
- title: Tiago Araujo
  url: https://ssw.com.au/people/tiago-araujo
related: []
redirects:
- do-you-underline-links-(and-include-a-rollover)

---

Always make links perfectly clear.

<!--endintro-->

It's very important that your links stand out from the background as well as the surrounding text. A solid underline and a contrasting color is the usually the best choice, but the exact method is not important as long as the end result stands out. A link should not only be discoverable upon accidental hovering.

Rollovers are important as they offer visual feedback to a user that this link that will take them somewhere. While there is a myriad of ways to do this; you can't go wrong with an underline or border-bottom.
<dl class="badImage"><br><br>::: greybox<br>For more information on this, please <a href="https://www.ssw.com.au/" style="border-bottom:none;color:inherit;">go to SSW website</a>.<br><br>:::<br><br><dd>Bad Example: The link is hard to recognize<br></dd></dl><dl class="goodImage"><br><br>::: greybox<br>For more information on this, please <a href="https://www.ssw.com.au/">go to SSW website</a>. <br><br>:::<br><br><dd>Good Example: This link is obvious<br><br></dd><p class="ssw15-rteElement-GreyBox"> 
      <img src="link-hover.jpg" alt="link-hover.jpg" data-pin-nopin="true"> <br></p><p class="ssw15-rteElement-P"></p><br><br>::: good<br>Good Example: Obvious rollover. You can test it by hovering the links on the example above<br><br>:::<br><br></dl>
Example CSS for rollover:
<dl class="image"><dt><p class="ssw15-rteElement-CodeArea">a:hover { <br>    color: #cc4141;<br>    cursor: pointer;<br>} <br></p></dt><dd>Figure: Example CSS for rollover effect <br></dd></dl>
