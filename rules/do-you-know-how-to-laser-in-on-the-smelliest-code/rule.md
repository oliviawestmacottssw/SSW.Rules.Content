---
type: rule
title: Do you know how to laser in on the smelliest code?
uri: do-you-know-how-to-laser-in-on-the-smelliest-code
created: 2012-03-16T08:36:31.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 23
  title: Damian Brady
- id: 24
  title: Adam Stephensen

---

 
Rather than randomly browsing for dodgy code, use Visual Studio's Code Metrics feature to identify "Hot Spots" that require investigation.

![467510-lotto-balls.jpeg](/SoftwareDevelopment/RulestobetterArchitectureandCodeReview/PublishingImages/lotto-balls.jpeg)
​Figure: The bad was is to browse the code

![](/SoftwareDevelopment/RulestobetterArchitectureandCodeReview/PublishingImages/VS%2011%20Code%20Metrics.png)
Figure: Run Code Metrics in VS11![](/SoftwareDevelopment/RulestobetterArchitectureandCodeReview/PublishingImages/CodeMetrics_3.png)
Figure: Red dots indicate the code that is hard to maintain e.g. Save() and LoadCustomer()

Identifying the problem areas is only the start of the process. From here, you should speak to the developers responsible for this dodgy code. There might be good reasons why they haven't invested time on this.
![Two devs talking](/SoftwareDevelopment/RulestobetterArchitectureandCodeReview/PublishingImages/two-devs-talking.jpg)Figure: Find out who the devs are by using the Annotate tool, and start a conversation.
**Tip: **To learn how to use Annotate, see [Do you know the benefits of Source Control?](http&#58;//www.ssw.com.au/ssw/Standards/Rules/RulesToBetterSourceControlwithTFS.aspx#UsingSourceControl).

Suggestion to MS: allow us to visualize the developers responsible for the bad code (currently and historically)
 
