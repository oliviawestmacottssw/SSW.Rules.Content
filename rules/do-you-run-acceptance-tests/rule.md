---
type: rule
title: Do You Run Acceptance Tests?
uri: do-you-run-acceptance-tests
created: 2012-08-01T15:07:10.0000000Z
authors:
- id: 24
  title: Adam Stephensen
- id: 1
  title: Adam Cogan

---

Once the coding is done by the developers, the functionality must then be stepped through in the required browsers. You can do this manually or automating it using a great tool like Microsoft Test Manager.

The 1st step in getting automated tests, is to setup Acceptance Tests:
 
![Run each 'test case' with a prescribed configuration](run-acceptance-tests-1.jpg)
![As you progress through each step, 'Pass' or 'Fail' the expected results. Take screen captures or video as appropriate](run-acceptance-tests-2.jpg)
[[badExample]]
| ![After checking all the ‘Expected’ results in your MTM test, do not forget to 'Pass' or 'Fail' the Test Case](run-acceptance-tests-3.jpg)
[[goodExample]]
| ![After all 'Test Steps' have been checked off, choose the overall status for the test. Otherwise it will continue to show as 'Active' on the reports](run-acceptance-tests-4.jpg)
[[badExample]]
| ![No Tests should remain as 'Active' or 'Failed' at the end of a Sprint](run-acceptance-tests-5.jpg)
[[goodExample]]
| ![every test is 'Passed'](run-acceptance-tests-6.jpg)
**Tip:**  You can pass a test from the test list. Select the Test menu, then the Test Suite. Choose the Test Case to pass and then click the green button ‘Pass Test’.

The next step is to        [review the Statistics of the Sprint](/Pages/How-to-Check-the-Status-of-the-Current-Sprint.aspx).
