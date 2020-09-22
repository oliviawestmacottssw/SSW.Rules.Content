---
type: rule
title: Do you use Live Unit Testing to see code coverage?
uri: do-you-use-live-unit-testing-to-see-code-coverage
created: 2020-03-12T23:43:11.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

 Visual Studio 2017 introduces a new feature called Live Unit Testing. This gives the developer insight into code coverage of the file that they are working on, so they can quickly and easily see if there’s a unit test that covers the code they are working on.
 ​![lut-codecoverage1.jpg](lut-codecoverage1.jpg)Figure: Enable it by selecting Test | Live Unit Testing | Start​![lut-codecoverage2.jpg](lut-codecoverage2.jpg)Figure: Bad Example – This method isn't covered by any unit tests, so the developer should consider writing a unit test for it​![lut-codecoverage3.jpg](lut-codecoverage3.jpg)Figure: The developer can right click and create a test immediately​![lut-codecoverage4.jpg](lut-codecoverage4.jpg)Figure: Good Example – Developer can see that the code is covered by 2 passing tests and one failing test
For more details see Joe Morris’s video on .NET Tooling Improvements Overview – Live Unit Testing:









​​

