---
type: rule
title: Do you know the common Design Principles? (Part 1)
uri: do-you-know-the-common-design-principles-part-1
created: 2012-04-02T00:29:11.0000000Z
authors:
- id: 24
  title: Adam Stephensen
- id: 23
  title: Damian Brady

---

 

| SRP​ | [​The Single Responsibility Principle](http&#58;//www.objectmentor.com/resources/articles/srp.pdf) | A class should have one, and only one, reason to change. |
| --- | --- | --- |
| OCP​ | [The Open Closed Principle​](http&#58;//www.objectmentor.com/resources/articles/ocp.pdf) | You should be able to extend a classes behaviour without modifying it.​ |
| --- | --- | --- |
| ​LSP | [The Liskov Substitution Principle​](http&#58;//www.objectmentor.com/resources/articles/lsp.pdf) | Derived classes must be substitutable for their base classes.​ |
| --- | --- | --- |
| ​ISP | [​The Interface Segregation Principle​](http&#58;//www.objectmentor.com/resources/articles/isp.pdf) | ​Make fine-grained interfaces that are client-specific.​ |
| --- | --- | --- |
| DIP​ | [The Dependency Inversion Principle​](http&#58;//www.objectmentor.com/resources/articles/dip.pdf) | Depend on abstractions, not on concretions.​ |
| --- | --- | --- |

Figure: Your code should be using SOLID principles
​It is assumed knowledge that you know these 6.
 If you don't, read about them on Uncle Bob's site above, or watch the [SOLID Pluralsight videos by Steve Smith.](http&#58;//www.pluralsight-training.net/microsoft/courses/TableOfContents?courseName=principles-oo-design&amp;highlight=)

## What order?

1. Look for Single Responsibility Principle violations. These are the most common and are the source of many other issues. Reducing the size and complexity of your classes and methods will often resolve other problems.
2. Liskov Substitution and Dependency Inversion are the next most common violations, so keep an eye out for them next.
3. When teams first begin implementing Dependency Injection, it is common for them to generate bloated interfaces that violate the Interface Segregation Principle.


After you have identified and corrected the most obvious broad principle violations, you can start drilling into code and looking for  localized code breaches. [ReSharper](http&#58;//www.jetbrains.com/resharper/) from JetBrains or [JustCode](http&#58;//www.telerik.com/products/justcode.aspx) from Telerik are invaluable tools once you get to this level.

Once you understand common design principles, look at [common design patterns](/SoftwareDevelopment/RulestobetterArchitectureandCodeReview/Pages/DoYouKnowCommonDesignPatterns.aspx) to help you follow them in your projects.

