---
type: rule
title: Do you know the tools you need before a "Test Please"?
uri: do-you-know-the-tools-you-need-before-a-test-please
created: 2009-02-26T02:44:26.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

 This field should not be null (Remove me when you edit this field). 
1. Perform automated testing with tools:
<br>    - SSW Link Auditor (for Web Apps) 
<br>    - SSW Code Auditor (for all Apps)
<br>    - SSW SQL Auditor (for all Apps with databases)
<br>    - SSW SQL Deploy's Reconcile (for all Apps with databases) 
<br>    - Visual Studio Team System Code Analysis (optional)
2. Perform automated testing via Unit Tests 
<br>    - nUnit (for Windows Apps), or
<br>    - Visual Studio Team System Unit Tests (for Web Apps)
3. Perform an internal "Test Please" (aka "Alpha Testing" e.g. only that pages or forms load, not checking the business rules)
4. Then send a "Test Please" to the client (aka "Acceptance Testing" to check the business rules)


