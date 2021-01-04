---
type: rule
archivedreason: 
title: Do you use MVC Unobtrusive Validation?
guid: efafaf89-9d76-42b2-8808-5403a8db6299
uri: do-you-use-mvc-unobtrusive-validation
created: 2013-12-12T05:01:16.0000000Z
authors:
- title: Brendan Richards
  url: https://ssw.com.au/people/brendan-richards
related: []
redirects: []

---

Validation is an important part of any data-driven web application. Client-Side validation provides fast user feedback and a better UI experience but cannot be relied on for data integrity - so client-side validation should always be backed by additional server-side validation.

With MVC Unobtrusive Validation, you can configure both client-side and server-side in one place.

<!--endintro-->

Validation rules can be added to a model object via Data Annotations or using the Fluent Validation API.

Fluent Validation is [available as a Nuget package](http://www.nuget.org/packages/FluentValidation/). See [Do you use Fluent Validation?](/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&TermId=fd57ceac-c551-44dc-b7c3-e6c348919f0d)
<dl class="image">&lt;dt&gt;<img src="DataAttributes.png" alt="DataAttributes.png">&lt;/dt&gt;<dd>Figure: OK Example - Data Annotation attributes decorate model properties to make them required</dd></dl><dl class="image">&lt;dt&gt;<img src="FluentValidation.png" alt="FluentValidation.png" style="width:650px;">&lt;/dt&gt;<dd>Figure: Better Example - Fluent Validation allows validation metadata to be added to a class without modifying the original class.  This provides much more flexibility for code reuse</dd></dl>
If you create a new MVC web application in VisualStudio 2013, unobtrusive validation will be enabled by default. Otherwise, it's simple to [install from Nuget](http://www.nuget.org/packages/Microsoft.jQuery.Unobtrusive.Validation/). To use it simply:

1. Bind your razor views to model objects
2. Use Html Helpers to render the form UI

<dl class="goodImage"> &lt;dt&gt;<img src="view.png" alt="view.png">&lt;/dt&gt;<dd>Figure: Good Example - this razor view binds to a strongly typed model object and uses HTML helpers.</dd></dl><dl class="image">&lt;dt&gt;<img src="Html.png" alt="Html.png" style="width:650px;">&lt;/dt&gt;<dd>Figure: the HTML UI rendered for this view now has data-validation attributes that are followed by JQuery validation to provide rich client-side validation.</dd></dl><dl class="image">&lt;dt&gt;<img src="SaveAction.png" alt="SaveAction.png">&lt;/dt&gt;<dd>Figure: On the server-side, the same validation rules will be checked when you call ModelState.IsValid</dd></dl>
