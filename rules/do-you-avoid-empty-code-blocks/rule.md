---
type: rule
archivedreason: 
title: Do you avoid Empty code blocks?
guid: 87d8d6e4-deba-44bf-a5db-4cc8b2c937b5
uri: do-you-avoid-empty-code-blocks
created: 2018-04-30T22:08:47.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
related: []
redirects: []

---


<p>​Empty Visual C# .NET method consumes program resources unnecessarily. Put a ​​comment in code block if its stub for future application.<br></p><p><strong>Exception&#58;</strong>&#160;If a Class implements an Inherited Interface method, you should add a comment within the Code block <br></p><br>
<br><excerpt class='endintro'></excerpt><br>
<p class="ssw15-rteElement-CodeArea">​public class Example<br> &#123;<br> public double salary()<br> &#123; 
   <br> &#125;<br> &#125;</p><dd class="ssw15-rteElement-FigureBad">​​Figure&#58; Bad Example - Method is empty​​​​​<br></dd><p class="ssw15-rteElement-CodeArea">​public class Sample<br> &#123;<br> public double salary()<br> &#123;<br> return 2500.00;<br> &#125;<br> &#125;</p><dd class="ssw15-rteElement-FigureGood">​Figure&#58; G​ood Example - Method implements some code<br></dd><p class="ssw15-rteElement-CodeArea">

public interface IDemo<br> &#123;<br> void DoSomethingUseful();<br> void SomethingThatCanBeIgnored();<br> &#125;<br>public class Demo &#58; IDemo<br> &#123;<br> public void DoSomethingUseful()<br> &#123;<br> // no audit issues<br> Console.WriteLine(&quot;Useful&quot;);<br> &#125;<br> // audit issues <br> public void SomethingThatCanBeIgnored()<br> &#123; <br> &#125; <br> &#125; </p><dd class="ssw15-rteElement-FigureBad">​Figure&#58; Bad Example - No Comment within empty code block</dd><p class="ssw15-rteElement-CodeArea">​​​public interface IDemo<br> &#123;<br> void DoSomethingUseful();<br> void SomethingThatCanBeIgnored();<br> &#125;<br>public class Demo &#58; IDemo<br> &#123;<br> public void DoSomethingUseful()<br> &#123;<br> // no audit issues<br> Console.WriteLine(&quot;Useful&quot;);<br> &#125;<br> // No audit issues <br> public void SomethingThatCanBeIgnored() <br> &#123;<br> // stub for IDemo interface<br> &#125; <br> &#125; </p><dd class="ssw15-rteElement-FigureGood">​​​Figure&#58; Good Example - Added comment within Empty Code block method of interface&#160;class</dd>​<br>


