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


If a client says:

*"This application is too slow, I don't really want to put up with such poor performance. Please fix."*

We don't jump in and look at the code and clean it up and reply with something like:

*"I've looked at the code and cleaned it up - not sure if this is suitable - please tell me if you are OK with the performance now."*

A better way is:

- Ask the client to tell us how slow it is (in seconds) and how fast they ideally would like it (in seconds)<br>
- Add some code to record the time the function takes to run<br>
- Reproduce the steps and record the time<br>
- Change the code<br>
- Reproduce the steps and record the time again<br>
- Reply to the customer:
 "It was 22 seconds, you asked for around 10 seconds. It is now 8 seconds."

![ ](/Management/RulesToSuccessfulProjects/PublishingImages/Code-Auditor-performance.jpg) Figure: Good example – Add some code to check the timing, before fixing any performance issues (An example from SSW Code Auditor)
This is because performance is an emotional thing, sometimes it just \*feels\* slower. Without numbers, a person cannot really know for sure whether something has become quicker.

#### Related

For sample code on how to measure performance for windows application form, please refer to rule [Do you have tests for Performance?](http&#58;//www.ssw.com.au/ssw/Standards/Rules/RulesToBetterUnitTests.aspx#Performance) on [Rules To Better Unit Tests](http&#58;//www.ssw.com.au/ssw/Standards/Rules/RulesToBetterUnitTests.aspx).

### Related Rule​

- ​Do you keep your website loading time acceptable?​


