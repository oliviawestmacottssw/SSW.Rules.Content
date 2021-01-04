---
type: rule
archivedreason: 
title: Do you provide alternate sizings for Bootstrap columns?
guid: 9b511eb2-12a1-44e5-9ece-980db19344bf
uri: do-you-provide-alternate-sizings-for-bootstrap-columns
created: 2014-06-18T05:04:12.0000000Z
authors:
- title: Ben Cull
  url: https://ssw.com.au/people/ben-cull
- title: Drew Robson
  url: https://ssw.com.au/people/drew-robson
related: []
redirects: []

---


<span style="line-height:20.799999237060547px;">​​​​​​Bootstrap provides a powerful, responsive layout with its rows and columns.</span>
<br><excerpt class='endintro'></excerpt><br>
<p>The common way to use Bootstrap's layout system is to create a basic grid which will appear as horizontal columns on the desktop but then stack on a smaller screen such as mobiles. This is done with a single set of .col-md-* classes.</p><dl class="badImage"><dt>
      <img src="23-06-2014 12-47-33 PM.png" alt="" style="width:400px;" /> 
   </dt><dd>Figure: Bad example - create the default stacking layout with Bootstrap</dd></dl><dl class="badImage"><dt>
      <img src="23-06-2014 1-04-08 PM.png" alt="23-06-2014 1-04-08 PM.png" style="margin:5px;" />
   </dt><dd>Figure:​ Bad example - the default stacking behavior on small devices</dd></dl><p>Did you know you can have more control over the responsive layout by including multiple column classes? The ability to control the layout across multiple screen sizes is a powerful tool within Bootstrap. For example, if you don't want your columns to stack on smaller devices, use the smaller grid classes by adding additional column classes (e.g. .col-xs-* .col-sm-*) to the respective <div>s. </p><dl class="goodImage"><dt>
      <img src="23-06-2014 12-45-30 PM.png" alt="23-06-2014 12-45-30 PM.png" style="width:400px;" />
   </dt><dd>Figure: Good example - add additional column classes to your columns</dd></dl><dl class="goodImage"><dt>
      <img src="23-06-2014 1-14-39 PM.png" alt="23-06-2014 1-14-39 PM.png" style="margin:5px;" />
   </dt><dd>​Figure: Good example - On a smaller device, these columns now arrange horizontally as desired</dd></dl>


