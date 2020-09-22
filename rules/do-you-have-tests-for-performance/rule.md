---
type: rule
title: Do you have tests for Performance?
uri: do-you-have-tests-for-performance
created: 2020-03-12T19:58:01.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

 ​Typically there are User Acceptance Tests that need to be written to measure the performance of your application. As a general rule of thumb, Forms should not load in more than 4 seconds. This can be automated with your unit testing framework.
 
**​Sample Code:**

public abstract class FormTestBase&lt;F&gt;
 where F : Form, new()
 {
 protected TimeSpan \_ExpectedLoadTime = TimeSpan.FromSeconds(4);
 [Test]
 public void LoadTest()
 {
 Stopwatch stopwatch = new Stopwatch();
 stopwatch.Start();
 F testForm = new F();
 testForm.Show();
 testForm.Close();
 stopwatch.Stop();
 Console.WriteLine("Form [{0}] took {1:#,##0.0} seconds to open", typeof(F), stopwatch.Elapsed.TotalSeconds);
 Assert.IsTrue(stopwatch.Elapsed &lt; \_ExpectedLoadTime, 
 string.Format("Loading time ({0:#,##0.0} seconds) exceed the expected time ({1:#,##0.0} seconds).", 
 stopwatch.Elapsed.TotalSeconds, \_ExpectedLoadTime.TotalSeconds));
 }
 }
 
 [TestFixture]
 public class LoginFormTests : FormTestBase&lt;LoginForm&gt;
 {
 }

 [TestFixture]
 public class MainFormTests : FormTestBase&lt;MainForm&gt;
 {
 }
​Figure: This code tests that the LoginForm and MainForm load in under 4 seconds​

