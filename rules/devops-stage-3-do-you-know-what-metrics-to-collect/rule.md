---
type: rule
archivedreason: 
title: 'DevOps – Stage 3: Do you know what metrics to collect?'
guid: 7867c4c4-1830-4cac-b42e-4926645c898b
uri: devops-stage-3-do-you-know-what-metrics-to-collect
created: 2016-03-07T18:22:18.0000000Z
authors:
- title: Eric Phan
  url: https://ssw.com.au/people/eric-phan
- title: Matt Wicks
  url: https://ssw.com.au/people/matt-wicks
related: []
redirects: []

---


<p class="p1">Now that your team is spending less time deploying the application, you’ve got more time to improve other aspects of the application, but first you need to know what to improve.&#160;​</p><p class="p1">Here are a few easy things to gather metrics on&#58;​</p>
<br><excerpt class='endintro'></excerpt><br>
<p></p><h3 class="ssw15-rteElement-H3">App​lication Logging (Exceptions)</h3><p class="ssw15-rteElement-P">See how many errors are being produced, aim to reduce this as the produce matures</p><p></p><ul><li><a href="/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=8c5a1235-d169-4164-92a1-08812c26fc22" style="line-height&#58;1.6;"><span class="s3">​​​​https&#58;//rules.ssw.com.au/do-you-use-the-best-exception-handling-library</span></a><br></li><li><span style="line-height&#58;1.6;">RayGun.io</span><br></li><li><span style="line-height&#58;1.6;">Application Insights​</span><br></li><li><span style="line-height&#58;1.6;"><a href="https&#58;//www.hockeyapp.net/">HockeyApp ​</a>(for mobile)</span></li></ul><p></p><p><span style="line-height&#58;1.6;">But it's not only exceptions you should be looking at but also how your users are using the application, so you can&#160;see where you should invest your time</span></p><ul><li><span style="line-height&#58;1.6;">Application Insights - https&#58;//rules.ssw.com.au/why-you-want-to-use-application-insights</span><br></li><li><span style="line-height&#58;1.6;">Google Analytics</span><br></li><li><span style="line-height&#58;1.6;">RayGun.io (Pulse)</span></li></ul><p></p><h3 class="ssw15-rteElement-H3">Application Metrics​</h3><p>Application/Server performance – track how your code is running in production, that way you can tell if you need to provision more servers or increase hardware specs to keep up with demand 
      </p><p></p><ul><li><span style="line-height&#58;1.6;">A</span><span style="line-height&#58;1.6;">pplic</span><span style="line-height&#58;1.6;">ation Insights - 
            </span><span class="s6" style="line-height&#58;1.6;"><a href="/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=6e9c1f28-fb3e-4a99-bcdf-363378e5da34">https&#58;//rules.ssw.com.au/rules-to-better-application-insights</a></span><br></li></ul><span class="s6"><dl class="image"><dt> 
                     <img src="/PublishingImages/appinsights.png" alt="appinsights.png" /> 
                  </dt></dl></span><p></p><p></p><ul><li><span style="line-height&#58;1.6;">​New r</span><span style="line-height&#58;1.6;">​</span><span style="line-height&#58;1.6;">elic</span><br></li></ul><dl class="image"><dt>
            <img src="/PublishingImages/newrelic.png" alt="newrelic.png" style="width&#58;808px;" />
            </dt></dl><p></p><ul><li><span style="line-height&#58;1.6;"><a href="https&#58;//www.hockeyapp.net/">Hockey App</a> (for mobile)</span><br></li></ul><p><span style="line-height&#58;1.6;background-color&#58;initial;"><img src="/SiteAssets/what-metrics-to-collect-stage-3/usermetrics-basic_users@2x.png" alt="usermetrics-basic_users@2x.png" style="margin&#58;5px;width&#58;808px;" />​</span></p><h3 class="ssw15-rteElement-H3">Process Metrics​</h3><p>​Collecting stats about the application isn't enough, you also need to be able to measure the time spent in the processes used to develop and maintain the application. You should keep an eye on and measure&#58;<br></p><ul><li><span style="line-height&#58;1.6;">​​Sprint Velocity</span><br></li><li><span style="line-height&#58;1.6;">Time spent in testing</span></li><li><span style="line-height&#58;1.6;">Time spent deployig</span></li><li><span style="line-height&#58;1.6;">Time spent getting a new developer up to speed</span></li><li><span style="line-height&#58;1.6;">Time spent in scrum ceremonies</span></li><li><span style="line-height&#58;1.6;">Time taken for a bug to be fixed and deployed to production</span></li></ul><h3 class="ssw15-rteElement-H3">​Code Metrics​<br></h3><p>The last set of metrics you should be looking at revolves around the code and how maintainable it is. You can use tools like&#58;<br></p><ul><li><span style="line-height&#58;20.8px;">Code Analaysis<br></span></li><li><span style="line-height&#58;20.8px;"><a href="https&#58;//www.codeauditor.com/">SSW Code Auditor</a></span></li><li><span style="line-height&#58;20.8px;"><a href="http&#58;//www.sonarqube.org/">SonarQube</a></span></li></ul><p></p><p></p>


