---
type: rule
title: Do you suffix unit test classes with "Tests"?
uri: do-you-suffix-unit-test-classes-with-tests
created: 2018-04-25T23:24:57.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

Unit test classes should be suffixed with the word "Tests" for better coding readability.
 
[TestFixture] public class SqlValidatorReportTest { }
Bad - Unit test class is not suffixed with "Tests"

[TestFixture] public class HtmlDocumentTests { }     
Good - Unit test class is suffixed with "Tests"

We have a program called [SSW Code Auditor](https&#58;//www.ssw.com.au/ssw/CodeAuditor/) to check for this rule.
