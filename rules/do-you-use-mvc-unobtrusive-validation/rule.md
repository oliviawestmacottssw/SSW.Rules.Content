---
type: rule
title: Do you use MVC Unobtrusive Validation?
uri: do-you-use-mvc-unobtrusive-validation
created: 2013-12-12T05:01:16.0000000Z
authors:
- id: 34
  title: Brendan Richards

---

 Validation is an important part of any data driven web application. Client-Side validation provides fast user feedback and a better UI experiance but cannot be relied on for data integrity - so cient-side validation should always be backup up with additional server-side validation.
With MVC Unobtrusive Valilidation, you can configure both client-side and server-side in one place.  
​Validation rules can be added to a model object via Data Annotations or using the Fluent Validation API. 
Fluent Validation is [available as a Nuget package](http&#58;//www.nuget.org/packages/FluentValidation/).

![DataAttributes.png](/SoftwareDevelopment/RulesToBetterMVC/PublishingImages/DataAttributes.png)
OK Example: Data Annotation attributes decorate model properties to make them required
![FluentValidation.png](/SoftwareDevelopment/RulesToBetterMVC/PublishingImages/FluentValidation.png)
Better Example: Fluent Validation allows validation meta data to be added to a class without modifying the original class.  This provides much more flexibility for code reuse.


If you create a new MVC web application in VisualStudio 2013, unobtrusive validation will be enabled by default. Otherwise it's simple to [install from Nuget​](http&#58;//www.nuget.org/packages/Microsoft.jQuery.Unobtrusive.Validation/). To use it simply:

1. Bind your razor views to model objects
2. Use Html Helpers to render the form UI​


![view.png](/SoftwareDevelopment/RulesToBetterMVC/PublishingImages/view.png)

Good Example: this razor view binds to a stronly typed model object and uses html helpers.



![Html.png](/SoftwareDevelopment/RulesToBetterMVC/PublishingImages/Html.png)
**Figure: the HTML UI rendered for this view now has data-validation attributes that are followed by JQuery validation to provide rich client-side validation.**




![SaveAction.png](/SoftwareDevelopment/RulesToBetterMVC/PublishingImages/SaveAction.png)


**Figure: On the server-side, the same validation rules will be checked when you call ModelState.IsValid**






