---
type: rule
title: Do you know the common Design Patterns? (Part 2 - Example)
uri: do-you-know-the-common-design-patterns-part-2---example
created: 2012-03-20T02:29:38.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 23
  title: Damian Brady
- id: 24
  title: Adam Stephensen
- id: 3
  title: Eric Phan

---

 
“Only add complexity <br>when you need flexibility” – Marcel de Vries
   ​Our controller is tightly coupled to the ExampleService and as a result, there is no way to unit test the controller.[This example is from the blog:[http://www.devtrends.co.uk/blog/how-not-to-do-dependency-injection-the-static-or-singleton-container](http&#58;//www.devtrends.co.uk/blog/how-not-to-do-dependency-injection-the-static-or-singleton-container) ]

| <br>`public` `class` `HomeController`<br><br>`{`<br><br>`    ``private` `readonly` `IExampleService _service;`<br><br>`    ` <br><br>`    ``public` `HomeController()`<br><br>`    ``{`<br><br>`      ``_service =``new` `ExampleService();`<br><br>`    ``}`<br><br>`    ` <br><br>`    ``public` `ActionResult Index()`<br><br>`    ``{`<br><br>`        ``return` `View(_service.GetSomething());`<br><br>`    ``}`<br><br>`}​`<br><br>`we have known this,how do we fix it?use container badly - without dependecy injection`<br><br>`public class HomeController
{
    private readonly IExampleService _service;
     
    public HomeController()
    {
      _service = Container.Instance.Resolve<IExampleService>();
    }
     
    public ActionResult Index()
    {
        return View(_service.GetSomething());
    }
}`<br> |
| --- |


[eg. Bad example - code showing NOT using dependency <br>injection]

This is bad because

1.we removed one coupling and adding another one(the container).

2.it's not very clear what's going on.(The beauty of dependency injection is that just by looking at the constructor of a class, you can tell exactly what it depends upon.)[Static IS THE](http&#58;//codebetter.com/patricksmacchia/2009/02/01/understanding-code-static-vs-dynamic-dependencies/)KEY:The idea I would like to defend now is that when it comes to
 understand and maintain a program, one need to focus mostly on thestatic dependencies, the ones found in
the source code.

use IoC correctly - with DI 



| <br>`public` `class` `HomeController`<br><br>`{`<br><br>`    ``private` `readonly` `IExampleService _service;`<br><br>`    ` <br><br>`    ``public` `HomeController(IExampleService service)`<br><br>`    ``{`<br><br>`      ``_service = service;`<br><br>`    ``}`<br><br>`    ` <br><br>`    ``public` `ActionResult Index()`<br><br>`    ``{`<br><br>`        ``return` `View(_service.GetSomething());`<br><br>`    ``}`<br><br>`}​`<br> |
| --- |


[eg. Good example - code showing using dependency <br>injection]










about overuse of patterns​

1.principles v.s. design patterns


| **SRP** | [The Single Responsibility Principle](http&#58;//www.objectmentor.com/resources/articles/srp.pdf) | *A class should have one, and only one, reason to change.* |
| --- | --- | --- |
| **OCP** | [The Open Closed Principle](http&#58;//www.objectmentor.com/resources/articles/ocp.pdf) | *You should be able to extend a classes behavior, without modifying it.* |
| **LSP** | [The Liskov Substitution Principle](http&#58;//www.objectmentor.com/resources/articles/lsp.pdf) | *Derived classes must be substitutable for their base classes.* |
| **DIP** | [The Dependency Inversion Principle](http&#58;//www.objectmentor.com/resources/articles/dip.pdf) | *Depend on abstractions, not on concretions.* |
| **ISP** | [The Interface Segregation Principle](http&#58;//www.objectmentor.com/resources/articles/isp.pdf) | *Make fine grained interfaces that are client specific.* |


Figure: 5 principles for class design

[[http://butunclebob.com/ArticleS.UncleBob.PrinciplesOfOod](http&#58;//butunclebob.com/ArticleS.UncleBob.PrinciplesOfOod)

&lt;&lt;[Agile Software Development, Principles, Patterns, and Practices](http&#58;//codebetter.com/davidhayden/2005/05/20/agile-software-development-principles-patterns-and-practices/)​&gt;&gt;Robert.C.Martin:

]





