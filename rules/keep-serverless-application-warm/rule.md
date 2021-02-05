---
type: rule
archivedreason: 
title: Do you keep your serverless application warm (to avoid cold starts)?
guid: ad45aab9-657e-4286-9799-209958ad11ed
uri: keep-serverless-application-warm
created: 2019-07-15T03:44:14.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
related: []
redirects:
- do-you-keep-your-serverless-application-warm-to-avoid-cold-starts
- do-you-keep-your-serverless-application-warm-(to-avoid-cold-starts)

---


When designing your Bot, you will very likely leverage some Bot Frameworks or AI Services to take care of the Natural Language Processing (NLP) so that you can focus on implementing your business logic.<br>To host your business logic, it is common to use serverless applications such as <a href="https&#58;//azure.microsoft.com/en-au/services/functions/">Azure Function</a>, <a href="https&#58;//firebase.google.com/">Google Firebase</a> or <a href="https&#58;//aws.amazon.com/lambda/">Amazon Web Service Lambda Functions</a>. Serverless applications come with amazing scaling abilities and simplified programming models, but they also suffer from at least one well-known side-effect that is commonly referred to as <strong>Cold Starts</strong>.&#160;&#160;<br>
<br><excerpt class='endintro'></excerpt><br>
<p><br></p>Here are some recommended solutions to eliminate Cold Starts&#58;<br>&#160;<br><strong style="font-size&#58;15px;">Microsoft Azure Functions</strong><br><ul><li><span style="color&#58;#333333;">​Add war</span><span style="color&#58;#333333;">m-up request</span></li></ul><p>&#160; &#160; &#160; &#160;Use a timer trigger function to keep the Azure Functions application warm. If you know that at a certain time of a day the Function App is likely to be cold and so you wake it up just before you expect users to send out requests.&#160;​​</p><ul><li><span style="color&#58;#333333;">Move to App Service Plan</span></li></ul>&#160; &#160; &#160; &#160;Azure Functions can be hosted using dedicated App Service Plans instead of the serverless Consumption plan. Now you no longer need to worry about cold starts since the compute resource is always available and ready. The only caveat is that the Azure Functions won't automatically scale out as they do with the Consumption plan. So, think ahead and measure your compute requirements, and make the right decision.<br>&#160;<br><ul><li>Upgrade to Premium Plan<br></li></ul>&#160; &#160; &#160; &#160;If you want a dedicated instance that is always available and ready, and you also require the ability to automatically scale out under high try the Azure Functions Premium Plan (preview). The premium plan always has at least 1 core ready to process requests and your application will not suffer from cold starts. The premium plan does come at a price, so plan ahead.<br>&#160;<div><br><span style="font-size&#58;15px;"><strong>Firebase Functions on Google Cloud Platform</strong></span><br><ul><li>In Node.js code, export all the functions your want to deploy to cloud functions. And import / require dependencies inside the function. So that each function call will only load the dependency it needs instead of loading all dependencies in the index.ts file.</li><li>​Warm up request - Create a separate function that works on a timer. The function can run at some time interval that you know your app will not be cold.</li><li>If cold starts are unbearable, convert to other infrastructure such as App Engine .</li></ul>&#160;<br><span style="font-size&#58;15px;"><strong>Amazon Web Service</strong></span><br><ul><li>Instead of using statically typed programming languages like Java and C#, you may prefer dynamically typed languages like Python, Node.js etc.</li><li>Avoid deploying Lambdas in Amazon Virtual Private Cloud (VPC).</li><li>Avoid making HTTPS or TCP client calls inside your lambda. Handshake or other security related calls are CPU bound and will increase the cold starts to your function.</li><li>Send dummy requests to your functions with some frequency.</li></ul><ol><li>Make necessary changes on your Lambda to distinguish warm-up calls from customer calls.</li><li>Be mindful about the potential drawbacks of the warm-up requests</li></ol>&#160;&#160;&#160;&#160;&#160;&#160;&#160; &#160; &#160; 2.1 Warm-up calls will potentially keep all your containers busy and a real customer request could not find a place to run<br>&#160; &#160; &#160; &#160; &#160; &#160; 2.2&#160;A Lambda function in one container can catch all calls at once and this can make other containers down after a while<br></div>


