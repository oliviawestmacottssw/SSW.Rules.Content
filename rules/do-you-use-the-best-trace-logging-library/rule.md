---
type: rule
title: Do you use the best trace logging library?
uri: do-you-use-the-best-trace-logging-library
created: 2013-09-11T21:38:08.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 38
  title: Drew Robson
- id: 34
  title: Brendan Richards

---

 
​The best trace logging framework is Log4Net.

Did you know that writing your own logging infrastructure code wastes time.

Log4net is a NuGet package that can be included in any .Net application, is easy to configure, supports many different output targets, has great performance, and allows for runtime changes to configuration.
 
It also supports the concept of logging at different levels of importance (e.g. Error, Warning, Information) and having different logs for different components of your application (e.g. a Customer Log and an Order Log).

For example, log4net allows you to support the following scenarios by making configuration changes in XML config files.

On all non-development machines:

- Write all Error Log Messages to the Windows Event Log, the database and email them to the administrators group
- Write all Warning messages to the database and email them to the administrators group
- Write all Information messages to the database, and email any information messages in the Order component to the Order Fulfilment team for them to check


On development machines:

- Write all Error Log Messages to the database
- Write all Warning messages to the database
- Write all Information messages on the area I am currently developing to the database

![](/SoftwareDevelopment/RulesForErrorHandling/PublishingImages/trace-logging-bad.jpg)Figure: Bad Example - Using Debug or Trace for logging, or writing hard coded mechanisms for logging does not allow you to configure logging at runtime![](/SoftwareDevelopment/RulesForErrorHandling/PublishingImages/trace-logging-bad-2.jpg)Figure: Bad Example - Roll your own logging components lack functionality, and have not been tested as thoroughly for quality or performance as log4net![](/SoftwareDevelopment/RulesForErrorHandling/PublishingImages/trace-logging-good.jpg)Figure: Good Example - Using log4net requires less work to install and configure than a roll-you-own logger, and provides many more features
Log4Net should be added to your project via the NuGet package manager.

