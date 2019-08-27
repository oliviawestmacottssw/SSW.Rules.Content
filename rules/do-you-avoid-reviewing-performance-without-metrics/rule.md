---
type: rule
title: Do you avoid reviewing performance without metrics?
uri: do-you-avoid-reviewing-performance-without-metrics
created: 2009-03-17T05:48:04.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 78
  title: Matt Wicks

---


​If a client says:

*"This application is too slow, I don't really want to put up with such poor performance. Please fix."*

We don't jump in and look at the code and clean it up and reply with something like:

*"I've looked at the code and cleaned it up - not sure if this is suitable - please tell me if you are OK with the performance now."*

A better way is:

- Ask the client to tell us how slow it is (in seconds) and how fast they ideally would like it (in seconds)
- Add some code to record the time the function takes to run
- Reproduce the steps and record the time
- Change the code
- Reproduce the steps and record the time again
- Reply to the customer:
"It was 22 seconds, you asked for around 10 seconds. It is now 8 seconds."

![ ](/PublishingImages/Code-Auditor-performance.jpg)Figure: Good example – Add some code to check the timing, before fixing any performance issues (An example from SSW Code Auditor)
Also, never forget to do incremental changes in your tests!

For example, if you are trying to measure the optimal number of processors for a server, do not go from 1 processor to 4 processors at once:
![1to4.png](/PublishingImages/1to4.png)Figure: Bad Example - Going from 1 to 4 all at once gives you incomplete measurements and data
Do it incrementally, adding 1 processor each time, measuring the results, and then adding more:
![1234.png](/PublishingImages/1234.png)Figure: Good Example - Going from 1 to 2, then measuring, then incrementally adding one more, measuring...
This gives you the most complete set of data to work from.

This is because performance is an emotional thing, sometimes it just \*feels\* slower. Without numbers, a person cannot really know for sure whether something has become quicker. By making the changes incrementally, you can be assured that there aren’t bad changes cancelling out the effect of good changes.​

### Samples​


For sample code on how to measure performance for windows application form, please refer to rule [Do you have tests for Performance?](http&#58;//www.ssw.com.au/ssw/Standards/Rules/RulesToBetterUnitTests.aspx#Performance) on [Rules To Better Unit Tests](http&#58;//www.ssw.com.au/ssw/Standards/Rules/RulesToBetterUnitTests.aspx).

### Related Rule

- [Do you keep your website loading ti​me acceptable?](/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=cb28d27b-542f-4f02-bfa4-31b3672ed0d5)​


