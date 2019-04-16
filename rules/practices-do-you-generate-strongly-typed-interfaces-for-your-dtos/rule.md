---
type: rule
archivedreason: 
title: Practices - Do you generate strongly-typed interfaces for your DTOs?
guid: 9b55d5cf-d6b9-4a49-92a5-fcaba2717040
uri: practices-do-you-generate-strongly-typed-interfaces-for-your-dtos
created: 2016-04-22T22:33:50.0000000Z
authors:
- title: Steve Leigh
  url: https://ssw.com.au/people/steve-leigh
- title: Brendan Richards
  url: https://ssw.com.au/people/brendan-richards
related: []
redirects: []

---

Inevitably, our well-engineered Angular application will need to send and receive data from a service of some sort – usually a Web API. A common mistake people make when doing this is using typescript’s built in  **any** type for these services, which offers no type safety whatsoever.

<!--endintro-->
<dl class="badImage">&lt;dt&gt; 
      <img alt="dtogs-bad.png" src="dtogs-bad.png"> 
   &lt;/dt&gt;<dd>Figure: Bad example - The "any" type is used as the DTO for this service. There is no type safety.</dd></dl>
One step better is to manually create interfaces for the DTOs. This gives type safety, but still means a lot of manual, tedious work to generate the interfaces.
<dl class="image">&lt;dt&gt; 
      <img alt="dtogs-ok.png" src="dtogs-ok.png"> 
   &lt;/dt&gt;<dd>Figure: OK example - Manually coded interface ensures any object passed to the service is in the correct format </dd></dl>
But this still doesn’t give safety over-the-wire – if the server side model changes, a developer has to remember to update it here, and hope that there are no typos.  This is also extra effort to perform something mindlessly repetitive – something a machine is much better at doing.  And we are programmers, right?
If your WebAPI has an OpenAPI (a.k.a. Swagger) specification, then the NSwag tools can build a complete Typescript client configured as an Angular injectable service - complete with: 

* HttpClient calls that return Observables
* All defined endpoints implemented as methods in the service
* All DTOs included as Typescript interfaces

<dl class="goodImage">&lt;dt&gt; 
         <img src="nswag.png" alt="" style="margin:5px;width:808px;"> 
      &lt;/dt&gt;<dd>Figure: Good example - NSwag generates the boring work so that you don't have to.<br></dd><p class="ssw15-rteElement-P"><br></p></dl>

![](northwind-client.png)


::: good
Figure: Good example: this client side api-access code from Jason Taylor's NorthwindTraders sample project has been generated by NSwag https://github.com/JasonGT/NorthwindTraders

:::