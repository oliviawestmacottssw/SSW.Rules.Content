---
type: rule
title: Do you use Thin controllers, Fat models and Dumb views?
uri: do-you-use-thin-controllers-fat-models-and-dumb-views
created: 2012-07-18T17:54:57.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

 
## Thin Controllers

You need to think of a controller as more of a coordinator than a controller. 
It is responsible for calling the business layer and passing from the business layer to the view. 
It is also responsible for process flow.
public ActionResult Details(decimal todaysWeather)
<br>{
<br>    var todaysWeatherInFarhenheit = ((9.0 / 5.0) \* todaysWeather) + 32;
<br>    return View(todaysWeatherInFarhenheit);<br> }
Figure: Business logic is mixed up within the controller making it fatter than it should bepublic ActionResult Index()
<br>{
<br>    var todaysWeather = weatherDB.Today.ToList();
<br>    return View(todaysWeather);
<br> }Figure: The controller is co-ordinating between the business layer and the viewpublic ActionResult Details(int? id)
<br> {
<br>   if (!id.HasValue)
<br>         return RedirectToAction("Index");

<br>   return View();
<br> }Figure: The controller is co-ordinating process flow (directing traffic)
## Dumb Views

Views shouldn't have any flow logic, application logic or business rules.
The only logic you should have in the view is in relation to the displaying of data.
The view should never go out and get information from somewhere else.
@{ var theMonth = DateTime.Now.Month; }
<br>&lt;p&gt;The numeric value of the current month: @theMonth&lt;/p&gt;

<br>@{
<br>    var outsidetempinfahrenheit = ((9.0 / 5.0) \* model.outsideTemp) + 32;
<br>    var weatherMessage = "Hello, it is " + outsidetempinfahrenheit + " 
degrees.";
<br>}
<br>&lt;p&gt;Today's weather: @weatherMessage&lt;/p&gt;Figure: Business logic is mixed in with the view@{ var theMonth = DateTime.Now.Month; }
<br>&lt;p&gt;The numeric value of the current month: @theMonth&lt;/p&gt;

<br>@{
<br>    var weatherMessage = "Hello, it is " + model.outsideTemp + " degrees.";
<br>}
<br>&lt;p&gt;Today's weather: @weatherMessage&lt;/p&gt;
Figure: The logic is related to the displaying of data only
## Fat Model

So where do we put all the logic? The answer of course is in the model, hence the name fat model.

