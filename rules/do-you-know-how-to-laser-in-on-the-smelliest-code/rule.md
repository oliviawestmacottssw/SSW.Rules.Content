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

 
Rather than randomly browsing for dodgy code, use Visual Studio's Code Metrics feature to identify "Hot Spots" that require investigation.

![](/SoftwareDevelopment/RulestobetterArchitectureandCodeReview/PublishingImages/VS%2011%20Code%20Metrics.png) 
Figure: Run Code Metrics in VS11



 ![](/SoftwareDevelopment/RulestobetterArchitectureandCodeReview/PublishingImages/CodeMetrics_3.png)

Figure: Red dots indicate the code that is hard to maintain e.g. Save() and LoadCustomer()
Identifying the problem areas is on the start of the process.  From here, you shoudl speak to the developers responsible for the dodgy code.

To find out who they are, use the Annotate tool. See [Do you know the benefits of Source Control?](http&#58;//www.ssw.com.au/ssw/Standards/Rules/RulesToBetterSourceControlwithTFS.aspx#UsingSourceControl) for more information.

 


Suggestion to MS: allow us to visualize the developers responsible for the bad code (currently and historically)
 
