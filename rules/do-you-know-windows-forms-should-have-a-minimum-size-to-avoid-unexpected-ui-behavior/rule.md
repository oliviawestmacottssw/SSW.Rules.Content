---
type: rule
archivedreason: 
title: Do you know Windows Forms should have a minimum size to avoid unexpected UI behavior
guid: 08de57ee-b4ff-4438-943b-5851b0da30fa
uri: do-you-know-windows-forms-should-have-a-minimum-size-to-avoid-unexpected-ui-behavior
created: 2015-06-30T08:31:56.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
related: []
redirects: []

---

If windows form does not setup a minimum size, your users could have unpredictable form behaviour as seen below:
<dt style="border:none;"><img alt="Bad window form" src="../../assets/Bugsize.gif" style="margin:5px;padding:15px;border:1px solid #cccccc;background:#eeeeee;">&lt;/dt&gt;<br><br>::: bad<br>Figure: Bad Example - Unexpected window form<br>:::<br><br><span style="line-height:20.7999992370605px;"><br></span></dt>

<!--endintro-->

Therefore, a standard has been built to ensure Windows forms have a minimum size.
<dt style="border:none;"><img alt="Good window form" src="../../assets/Minisize.gif" style="margin:5px;padding:15px;border:1px solid #cccccc;background:#eeeeee;">&lt;/dt&gt;<br><br>::: good<br>Figure: Good Example - User friendly window form<br>:::<br><br><p><br></p>
</dt>
