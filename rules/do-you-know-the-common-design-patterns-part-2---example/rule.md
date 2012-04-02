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

 
​Appropriate use of design patterns can ensure your code is maintainable.
 
Using the Dependency Injection pattern allows us to decrease the coupling of our classes.

For example: our controller is tightly coupled to the ExampleService and as a result, there is no way to unit test the controller.

[This example is from the blog: [http://www.devtrends.co.uk/blog/how-not-to-do-dependency-injection-the-static-or-singleton-container](http&#58;//www.devtrends.co.uk/blog/how-not-to-do-dependency-injection-the-static-or-singleton-container) ] 

| <br> <br><br>`public class HomeController{    private readonly IExampleService _service;    public HomeController()    {      _service = new ExampleService();    }         public ActionResult Index()    {        return View(_service.GetSomething());    }}​`<br><br>Figure: Bad example - Controller coupled with ExampleService<br><br>we have known this,how do we fix it?use container badly - without dependecy injection<br><br>`public class HomeController{    private readonly IExampleService _service;         public HomeController()    {      _service = Container.Instance.Resolve<IExampleService>();    }         public ActionResult Index()    {        return View(_service.GetSomething());    }}`<br> |
| --- |


 Figure: Bad example - 2nd attempt using an Inversion of Control container but \*not\* using dependency injection. A dependency now exists on the Container.

This is bad code because we removed one coupling but added another one (the container).

 



| <br>`public class HomeController{    private readonly IExampleService _service;         public HomeController(IExampleService service)    {      _service = service;    }         public ActionResult Index()    {        return View(_service.GetSomething());    }}​`<br> |
| --- |

Figure: Good example - code showing using dependency injection. No static dependencies. 


It is important to know when the use of a pattern is appropriate.  Patterns can be useful, but they can also be harmful if used incorrectly.



