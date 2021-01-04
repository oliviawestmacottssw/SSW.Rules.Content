---
type: rule
archivedreason: 
title: (Before starting) Do you follow a Test Driven Process?
guid: 786cd996-54da-4864-9362-26893d5acb4d
uri: before-starting-do-you-follow-a-test-driven-process
created: 2011-11-18T03:52:57.0000000Z
authors:
- title: Justin King
  url: https://ssw.com.au/people/justin-king
- title: Tristan Kurniawan
  url: https://ssw.com.au/people/tristan-kurniawan
related: []
redirects: []

---

Never allow a situation where a developer can check out code and the code does not compile – or the unit tests are not all green. This is called “breaking the build” and the punishment in our office is 20 push-ups and fixing broken links for an hour!   
<!--endintro-->
<dl class="bad">&lt;dt&gt;<ol><li>Check out</li><li>Compile</li><li>Develop</li><li>Compile</li><li>Check In</li></ol>&lt;/dt&gt;<dd>Figure: Bad example - wrong process</dd></dl><dl class="image">&lt;dt&gt; 
      <img src="BeforeCoding.jpg" alt=""> 
   &lt;/dt&gt;<dd>Figure: Before you start cooking prepare all your ingredients. Before you start coding, "Get Latest" the right way</dd></dl><dl class="good">&lt;dt&gt;<ol><li>Get latest </li><li>Compile </li><li>Run Unit Tests </li><li>If Tests pass then start developing </li><li>Check out </li><li>Develop </li><li>Compile </li><li>Run Unit Tests </li><li>Get Latest (Always do a Get Latest before checking in as code you didn't change could break your code) </li><li>Compile </li><li>Run Unit Tests </li><li>Check In if all tests passed </li><li>Wait for gated check-in (GC) to complete </li><li>Reconcile your workspace if it was successful </li><li>Check that Continuous Integration (CI) build was successful(If GC was skipped) </li></ol>&lt;/dt&gt;<dd>Figure: Good example - right process</dd></dl>
**Note:** You should have both a Gated-Check-in (GC) and a Continuous Integration (CI) build on every branch.
