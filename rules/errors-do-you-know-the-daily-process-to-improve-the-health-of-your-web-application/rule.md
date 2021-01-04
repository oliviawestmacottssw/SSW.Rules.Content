---
type: rule
archivedreason: 
title: Errors – Do you know the daily process to improve the health of your web application?
guid: a06a5bdd-7f6f-4b4f-8769-cd05ae890ce7
uri: errors-do-you-know-the-daily-process-to-improve-the-health-of-your-web-application
created: 2014-08-19T00:51:51.0000000Z
authors:
- title: Drew Robson
  url: https://ssw.com.au/people/drew-robson
- title: Chris Briggs
  url: https://ssw.com.au/people/chris-briggs
related: []
redirects: []

---


​​​​​​​Application Insights can provide an overwhelming amount of errors in your web application, so use just-in-time bug processing to handle them.<br>
<br><excerpt class='endintro'></excerpt><br>
<p>The goal is to each morning check your web application's dashboard and find zero errors. However, what happens if there are multiple errors? Don't panic, follow this process to improve your application's health.</p><dl class="image"><dt>
      <img src="App-Insights-Failures.png" alt="20-08-2014-11-50-59-AM-compressor.png" style="width:800px;" /> 
   </dt><dd>Figure: Every morning developers check Application Insights for errors​<br></dd></dl><p>Once you have found an exception you can drill down into it to discover more context around what was happening. You can find out the user's browser details, what page they tried to access, as well as the stack trace (Tip: make sure you follow the rule on <a href="/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&TermId=68f64a3a-78ec-49f6-87ed-7ee92af1c809">How to set up Application Insights</a> to enhance the stack trace).</p><dl class="image"><dt> 
      <img src="App-Insights-Failures-drilldown.png" alt="" style="width:800px;" /> 
   </dt><dd>Figure: Drilling down into an exception to discover more.</dd></dl><p>It's easy to be overwhelmed by all these issues, so don't create a bug for each issue or even the top 5 issues. Simply create one bug for the most critical issue. Reproduce, fix and close the bug then you can move onto the next one and repeat. This is just-in-time bug processing and will move your application towards better health one step at a time.</p><dl class="badImage"><dt> 
      <img src="20-08-2014-12-04-31-PM-compressor.png" alt="20-08-2014-12-04-31-PM-compressor.png" style="width:800px;" /> 
   </dt><dd>Figure: Bad example - creating all the bugs</dd></dl><dl class="goodImage"><dt>
      <img src="20-08-2014-12-06-16-PM-compressor.png" alt="20-08-2014-12-06-16-PM-compressor.png" style="width:800px;" />​<br></dt><dd>Figure: Good example - create the first bug (unfortunately bug has to be created manually)<br></dd></dl>


