---
type: rule
title: Do you use a logging framework?
uri: do-you-use-a-logging-framework
created: 2012-04-01T09:53:00.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 23
  title: Damian Brady
- id: 78
  title: Matt Wicks

---

 
Unless you are writing a Console application, any output that uses Console.WriteLine will almost certainly be lost.  You're much better off using Trace.WriteLine.

You can create a trace listener to send your Trace.WriteLine statements to the Console if you wish, but you can also redirect them elsewhere if required.  See [this MSDN article for more information](http&#58;//msdn.microsoft.com/en-us/library/sk36c28t.aspx).

Console.WriteLine("Service started"); Figure: Bad Example - Using Console.WriteLine to write debug information

Trace.WriteLine("Service started"); Figure: Good Example - Using Trace.WriteLine to write debug informatio
 
