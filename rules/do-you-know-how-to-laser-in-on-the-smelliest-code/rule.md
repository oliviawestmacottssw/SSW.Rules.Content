---
type: rule
archivedreason: 
title: Do you know how to laser in on the smelliest code?
guid: c69ca2e5-0323-430e-ae26-62a753d4ace5
uri: do-you-know-how-to-laser-in-on-the-smelliest-code
created: 2012-03-16T08:36:31.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 23
  title: Damian Brady
- id: 24
  title: Adam Stephensen
related: []
redirects: []

---

Rather than randomly browsing for dodgy code, use Visual Studio's Code Metrics feature to identify "Hot Spots" that require investigation.

![The bad was is to browse the code](lotto-balls.jpeg)

<!--endintro-->

![Run Code Metrics in Visual Studio](VS 11 Code Metrics.png)
![Red dots indicate the code that is hard to maintain. E.g. Save](CodeMetrics_3.png)() and LoadCustomer()
Identifying the problem areas is only the start of the process. From here, you should speak to the developers responsible for this dodgy code. There might be good reasons why they haven't invested time on this.

![Find out who the devs are by using CodeLens and start a conversation Tip: To learn how to use Annotate, see](codelens-start-conversation.png)[Do you know the benefits of Source Control?](http://www.ssw.com.au/ssw/Standards/Rules/RulesToBetterSourceControlwithTFS.aspx#UsingSourceControl)




::: greybox
 **Suggestion to Microsoft:** allow us to visualize the developers responsible for the bad code (currently and historically) using CodeLens.

:::
