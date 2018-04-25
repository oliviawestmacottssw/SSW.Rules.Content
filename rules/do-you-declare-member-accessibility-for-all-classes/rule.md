---
type: rule
archivedreason: 
title: Do you declare member accessibility for all classes?
guid: b1ac5f48-0e88-4eed-8a13-c25ca5a87c6a
uri: do-you-declare-member-accessibility-for-all-classes
created: 2018-04-25T22:45:00.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
related: []
redirects: []

---


<p class="ssw15-rteElement-P">Not explicitly specifying the access type for members of a structure or class can be deceiving for other developers that are using this structure or class. The default structure and class members access in Visual C# .NET is always private. The default class member access in Visual Basic .NET is private. However, the default structure member access in Visual Basic .NET is public. <br></p>
<br><excerpt class='endintro'></excerpt><br>
<p class="ssw15-rteElement-CodeArea">Match MatchExpression(string input, string pattern)&#160;</p><dd class="ssw15-rteElement-FigureBad">Figure&#58; Bad - Method without member accessibility declared <br></dd><p class="ssw15-rteElement-CodeArea">private Match MatchExpression(string input, string pattern)&#160;<br></p><dd class="ssw15-rteElement-FigureGood">Figure&#58; Good - Method with member accessibility declared</dd><p class="ssw15-rteElement-YellowBorderBox">We have a program called&#160;<a href="https&#58;//www.ssw.com.au/ssw/CodeAuditor/Rules.aspx#Interoper">SSW Code Auditor </a> to check for this rule. <br></p>


