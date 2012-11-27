---
type: rule
title: Controls - Do you use the fonts recommended by Microsoft in your application? (Windows Forms Only)
uri: controls---do-you-use-the-fonts-recommended-by-microsoft-in-your-application-windows-forms-only
created: 2012-11-27T09:16:16.0000000Z
authors: []

---

 
Some font are easier to read then others, at SSW we follow Microsoft's [Visual Design Guidelines](http&#58;//www.ssw.com.au/ssw/Redirect/Microsoft/MSDNInterfaceText.htm). This means we use Tahoma 8pt as our font of choice.
   ​
At SSW, we use Code Auditor to ensure all fonts on our forms are set to Tahoma but we allow controls to use a different font. This is because certain information is better displayed in a different font. For example a Textbox to show code should use Courier instead of Tahoma.
<dl class="badImage"><dt><img alt="Form with Arial Narrow Font" src="http&#58;//www.ssw.com.au/ssw/Standards/Rules/Images/FontBadArialNarrow.gif"></dt>
<dd>Figure&#58; Bad Example - This form uses a non-standard font, and it is hard to read</dd></dl><dl class="goodImage"><dt><img alt="Form with Tahoma Font" src="http&#58;//www.ssw.com.au/ssw/Standards/Rules/Images/FontGoodTahoma.gif"></dt>
<dd>Figure&#58; Good Example - This form uses Tahoma, and it is easy to read</dd></dl><dl class="goodImage"><dt><img alt="Form with Tahoma Font, and a RichTextBox with Courier New Font" src="http&#58;//www.ssw.com.au/ssw/Standards/Rules/Images/FontCourierNew.gif"></dt>
<dd>Figure&#58; Good Example - This form uses Tahoma, and the RichTextBox displays source code using Courier New</dd></dl>

| We have a program called [SSW Code Auditor](http&#58;//www.ssw.com.au/ssw/CodeAuditor/Rules.aspx#VBFont) to check for this rule. |
| --- |


