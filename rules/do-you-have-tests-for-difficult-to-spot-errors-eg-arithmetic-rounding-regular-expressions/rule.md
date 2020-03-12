---
type: rule
archivedreason: 
title: Do you have tests for difficult to spot errors - e.g. Arithmetic, Rounding, Regular Expressions?
guid: 8bb8ec43-680b-4610-8ffc-0cd9c559b03b
uri: do-you-have-tests-for-difficult-to-spot-errors-eg-arithmetic-rounding-regular-expressions
created: 2020-03-12T19:51:40.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
related: []
redirects: []

---


By difficult to spot errors we mean errors that do not give the user a prompt that an error has occurred. Things such as&#58; Arithmetic, Rounding or Calculations should have unit tests written for them.<br>
<br><excerpt class='endintro'></excerpt><br>
<p>Sample Code&#58;</p><p class="ssw15-rteElement-CodeArea">DataAccess |Utilities.cs<br>using System;<br>using System.Collections.Generic;<br>using System.Text;<br>namespace DataAccess &#123;<br> public class Utilities &#123;<br> // A business rule – it should be unit tested<br> public decimal CalculateTotal(List&lt;myitem&gt; items) &#123;<br> decimal total = 0.0M;<br> foreach (MyItem i in items) &#123;<br> total += i.UnitPrice * (1 - i.Discount);<br> &#125;<br> return total;<br> &#125; <br> &#125;<br>&#125;</p><dd class="ssw15-rteElement-FigureNormal">​Figure&#58; Function to calculate a total for a list of items</dd><p class="ssw15-rteElement-P">For a func​​tion like this, it might be simple to spot errors when there are one or two items, but if you were to calculate the total for 50 items, then the task of spotting an error isn't so easy. That's why a unit test should be written so that you know when the function doesn't work.</p><p><b>Sample Test&#58;</b></p><p class="ssw15-rteElement-CodeArea">DataAccess.Tests | UtilitiesTest.cs<br>using System;<br>using System.Collections.Generic;<br>using System.Text;<br>using NUnit.Framework;<br>namespace DataAccess.Tests &#123;<br> [TestFixture()]<br> public class UtilitiesTests &#123;<br> [Test()]<br> public void CalculateTotalSimpleTest() &#123;<br> List&lt;myitem&gt; items = new List&lt;MyItem&gt;();<br> items.Add(new MyItem(12.50M));<br> items.Add(new MyItem(4.75M));<br> items.Add(new MyItem(9.05M));<br> items.Add(new MyItem(6.55M));<br> items.Add(new MyItem(20.12M));<br> decimal expected = 52.97M;<br> Utilities u = new Utilities();<br> decimal actual = u.CalculateTotal(items);<br> Assert.AreEqual(expected, actual);<br> &#125;<br> [Test()]<br> public void CalculateTotalWithDiscountTest() &#123;<br> List&lt;myitem&gt; items = new List&lt;myitem&gt;();<br> items.Add(new MyItem(12.50M, 0.1M));<br> items.Add(new MyItem(4.75M));<br> items.Add(new MyItem(9.05M));<br> items.Add(new MyItem(6.55M));<br> items.Add(new MyItem(20.12M));<br> decimal expected = 51.72M;<br> Utilities u = new Utilities();<br> Assert.IsNotNull(u);<br> decimal actual = u.CalculateTotal(items);<br> Assert.AreEqual(expected, actual);<br> &#125;<br> &#125;<br>&#125;<br>DataAccess | MyItem.cs<br>using System;<br>using System.Collections.Generic;<br>using System.Text;<br>namespace DataAccess &#123;<br> public class MyItem &#123;<br> public MyItem(decimal unitPrice) &#123;<br> _unitPrice = unitPrice;<br> &#125;<br> public MyItem(decimal unitPrice, decimal discount) &#58; this(unitPrice) &#123;<br> _discount = discount;<br> &#125;<br> private decimal _unitPrice;<br> private decimal _discount;<br> public decimal Discount &#123;<br> get &#123; return _discount; &#125;<br> set &#123; _discount = value; &#125;<br> &#125;<br> public decimal UnitPrice &#123;<br> get &#123; return _unitPrice; &#125;<br> set &#123; _unitPrice = value; &#125;<br> &#125;<br> &#125;<br>&#125;</p><dd class="ssw15-rteElement-FigureNormal">​Figure&#58; Test calculates total by checking something we know the result of. (Note&#58; it doesn't need a failure case because it isn't a Regex.)​<br></dd>


