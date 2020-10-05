---
type: rule
title: Do you use the CSS class "form horizontal" to arrange your fields and labels?
uri: do-you-use-the-css-class-form-horizontal-to-arrange-your-fields-and-labels
created: 2014-09-08T20:59:34.0000000Z
authors:
- id: 38
  title: Drew Robson

---

You should align labels **next** to the inputs on medium and large displays and **above** inputs on small and extra-small displays.
 
Bootstrap makes this easy. Use the css class **form-horizontal **on your html form for it to use this behaviour by default.
 
&lt;form class="form-horizontal"&gt;
    &lt;div class="form-group"&gt;
        &lt;label for="inputEmail3" class="col-sm-2 control-label"&gt;Email&lt;/label&gt;
        &lt;div class="col-sm-10"&gt;
            &lt;input type="email" class="form-control" id="inputEmail3" placeholder="Email"&gt;
        &lt;/div&gt;
    &lt;/div&gt;
    &lt;div class="form-group"&gt;
        &lt;label for="inputPassword3" class="col-sm-2 control-label"&gt;Password&lt;/label&gt;
        &lt;div class="col-sm-10"&gt;
            &lt;input type="password" class="form-control" id="inputPassword3" placeholder="Password"&gt;
        &lt;/div&gt;
    &lt;/div&gt;
&lt;/form&gt;
Figure: Example html using Bootstrap to get the above behaviour
​See [http://getbootstrap.com/css/#forms-horizontal](http&#58;//getbootstrap.com/css/#forms-horizontal) for more information.

### Related Rule



- [Do you know how to arrange forms?](/do-you-know-how-to-arrange-forms)
