---
type: rule
archivedreason: 
title: Do you know the common Design Principles? (Part 1)
guid: 7507df2f-e227-4ecf-931f-4864ad85eb02
uri: do-you-know-the-common-design-principles-part-1
created: 2012-04-02T00:29:11.0000000Z
authors:
- title: Adam Stephensen
  url: https://ssw.com.au/people/adam-stephensen
- title: Damian Brady
  url: https://ssw.com.au/people/damian-brady
related: []
redirects: []

---


<p><table style="border-bottom&#58;#444 1px solid;border-left&#58;#444 1px solid;border-top&#58;#444 1px solid;border-right&#58;#444 1px solid;"><tbody><tr class="ssw-rteTableEvenRow-default"><th class="ssw-rteTableFirstCol-default" style="padding-right&#58;10px;">SRP​</th>
<td class="ssw-rteTableOddCol-default"><a href="http&#58;//www.objectmentor.com/resources/articles/srp.pdf">​The Single Responsibility Principle</a></td>
<td class="ssw-rteTableEvenCol-default">A class should have one, and only one, reason to change.</td></tr>
<tr class="ssw-rteTableOddRow-default"><th class="ssw-rteTableFirstCol-default" style="padding-right&#58;10px;">OCP​</th>
<td class="ssw-rteTableOddCol-default"><a href="http&#58;//www.objectmentor.com/resources/articles/ocp.pdf">The Open Closed Principle​</a></td>
<td class="ssw-rteTableEvenCol-default">You should be able to extend a classes behaviour without modifying it.​</td></tr>
<tr class="ssw-rteTableEvenRow-default"><th class="ssw-rteTableFirstCol-default" style="padding-right&#58;10px;">​LSP</th>
<td class="ssw-rteTableOddCol-default"><a href="http&#58;//www.objectmentor.com/resources/articles/lsp.pdf">The Liskov Substitution Principle​</a></td>
<td class="ssw-rteTableEvenCol-default">Derived classes must be substitutable for their base classes.​</td></tr>
<tr class="ssw-rteTableOddRow-default"><th class="ssw-rteTableFirstCol-default" style="padding-right&#58;10px;">​ISP</th>
<td class="ssw-rteTableOddCol-default"><a href="http&#58;//www.objectmentor.com/resources/articles/isp.pdf">​The Interface Segregation Principle​</a></td>
<td class="ssw-rteTableEvenCol-default">​Make fine-grained interfaces that are client-specific.​</td></tr>
<tr class="ssw-rteTableEvenRow-default"><th class="ssw-rteTableFirstCol-default" style="padding-right&#58;10px;">DIP​</th>
<td class="ssw-rteTableOddCol-default"><a href="http&#58;//www.objectmentor.com/resources/articles/dip.pdf">The Dependency Inversion Principle​</a></td>
<td class="ssw-rteTableEvenCol-default">Depend on abstractions, not on concretions.​</td></tr></tbody></table></p>
<div class="ssw-rteStyle-FigureNormal">Figure&#58; Your code should be using SOLID principles</div>
<br><excerpt class='endintro'></excerpt><br>
<p>​It is assumed knowledge that you know these 6. If you don't, read about them on Uncle Bob's site above, or watch the <a href="http&#58;//www.pluralsight-training.net/microsoft/courses/TableOfContents?courseName=principles-oo-design&amp;highlight=">SOLID Pluralsight videos by Steve Smith.</a></p>
<p><strong>What order?</strong></p>
<ol><li>Look for Single Responsibility&#160;Principle violations. These are the most common and are the source of many other issues. Reducing the size and complexity of your classes and methods will often resolve other problems.</li>
<li>Liskov Substitution and Dependency Inversion are the next most common violations, so keep an eye out for them next.</li>
<li>When teams first begin implementing Dependency Injection, it is common for them to generate bloated interfaces that violate the Interface Segregation Principle.</li></ol>
<p>After you have identified and corrected the most obvious broad principle violations, you can start drilling into code and looking for&#160; localized code breaches. <a href="http&#58;//www.jetbrains.com/resharper/">ReSharper</a> from JetBrains or&#160;<a href="http&#58;//www.telerik.com/products/justcode.aspx">JustCode</a> from Telerik&#160;are invaluable tools once you get to this level.</p>
<p>Once you understand common design principles, look at <a href="/SoftwareDevelopment/RulestobetterArchitectureandCodeReview/Pages/DoYouKnowCommonDesignPatterns.aspx">common design patterns</a> to help you follow them in your projects.</p>


