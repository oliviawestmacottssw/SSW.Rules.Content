---
type: rule
archivedreason: Rule is dated. Broken apart into individual rules
title: Do you use the new C# 7 language features to slash the amount of boilerplate code you write?
guid: a1f628a2-b249-4057-bb34-74280db06e8f
uri: do-you-use-the-new-c-7-language-features-to-slash-the-amount-of-boilerplate-code-you-write
created: 2018-04-30T22:39:55.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
related: []
redirects: []

---


<p>​Up until this point, .NET developers had to write a lot of boilerplate code in order to properly format strings or check for null. This boilerplate code required a lot of work to ensure code readability and maintainability.<br></p><p>The new C# 6 that comes with Visual Studio 2015 is a game changer that empowers devs to do more with less.</p><p>These 3 features will slash the amount of boilerplate code you have to write and improve code quality&#58;​​<br></p><br>
<br><excerpt class='endintro'></excerpt><br>
<ol><li>nameof expressions - allows us to get the name of the type of object<p>Now when we throw an exception, we can use the name of expressions feature to create robust code, which is more resistant to common mistakes when refactoring. This is achieved by reducing the amount of hard coding.</p><p>As you can see, when in the past you would have to write the following code&#58;</p><p class="ssw15-rteElement-CodeArea">(if customer.Address.ZipCode == null) throw new ArgumentNullException(&quot;ZipCode&quot;);</p><dd class="ssw15-rteElement-FigureBad">Figure&#58; Bad example - Amount of boiler plate code for a simple task&#160; <br> </dd><p>Now you only have write&#58;</p><p class="ssw15-rteElement-CodeArea">(if customer.Address.ZipCode == null) throw new ArgumentNullException(nameof(customer.Address.ZipCode));</p><dd class="ssw15-rteElement-FigureGood">Figure&#58; Good example - The same functionality as the Bad Example in a single line of code</dd> The benefit of this change is when refactoring our code, we don't need to worry about searching for magic strings. Which common slip through the cracks and lead to confusing error messages.</li><li>String Interpolation - greatly reduces the amount of boilerplate code required when working with strings</li><p>Formatting strings on the fly was previously a task which required a stack of boilerplate code. In the Visual Studio 2015, we can use the smart String Interpolation feature. Not only does this feature reduce the amount of code we have to write, it also improves code readability.</p><p>For example, before C# 6, we would write&#58;</p><p class="ssw15-rteElement-CodeArea">var s = String.Format(&quot;Profit is $&#123;0&#125; this year&quot;, p.TotalEarnings - p.Totalcost);</p><dd class="ssw15-rteElement-FigureBad">Figure&#58; Bad example - Using the string format make the code difficult to read <br></dd><p>Now we are able to&#58;</p><p class="ssw15-rteElement-CodeArea">var s = &quot;Profit is $&#123;p.TotalEarnings - p.Totalcost&#125; this year&quot;;</p><dd class="ssw15-rteElement-FigureGood">Figure&#58; Good example - Very human readable code <br></dd>
   <p>As can be seen above by making use of the new String Interpolation feature, the understandability of your code is greatly improved.</p><li>​Null-conditional operators - makes checking for null as easy as inserting a single question mark<p>This great new feature has had a raft of positive reactions from developers. The new Null-conditional operators feature boils down all of the previously laborious clunky code into a single question mark.<br></p><p>For example, previously we would of had to write a chunk of code to achieve a simple task</p><p class="ssw15-rteElement-CodeArea">if(customers.Length != null) &#123; int length = customers.Length; &#125; else &#123; int length = 0; &#125;</p><dd class="ssw15-rteElement-FigureBad"><ul>Figure&#58; Bad example - Fragile code</ul></dd><p>Now we are able to replace that chunk of code with a single line</p><p class="ssw15-rteElement-CodeArea">int length = customers?.Length ?? 0;</p><dd class="ssw15-rteElement-FigureGood">Figure&#58; Good example - Robust code <br></dd><p>The promise In short, these new features will save you time, and help you write cleaner, more robust code - what's not to love?</p></li></ol>


