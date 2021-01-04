---
type: rule
archivedreason: This applies to WinForms applications. Modern desktop applications should follow MVVM or MVC - in which case the viewmodel/controller is unit testable on every commit.
title: Do you have a standard 'Help' menu that includes a way to run your unit tests?
guid: f87286af-173f-4603-8a32-28ce0f3eb0f0
uri: do-you-have-a-standard-help-menu-that-includes-a-way-to-run-your-unit-tests
created: 2020-03-12T23:07:16.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
related: []
redirects: []

---


<p class="ssw15-rteElement-P">Your standard help menu should include an option to run your Unit Tests. Everybody knows the importance of Unit tests for the middle tier. However, Unit Tests are also important to capture problems that occur on other peoples' machines so that users can perform a quick check when a product is not behaving correctly. This is important for troubleshooting during support calls and enables your customers to do a Health Check on the product.</p><p class="ssw15-rteElement-P">And yes, there are many tests that can be written that will pass on the developers PC - but not on the users PC. e.g. Ability to write to a directory, missing dlls, missing tables in the schema etc.​​<br></p>
<br><excerpt class='endintro'></excerpt><br>
<p>
   <b>Note:</b> Adding this option requires you to include NUnit in your setup.exe (See <a href="https://www.ssw.com.au/ssw/Standards/WiseSetup/WiseStandards.aspx#IncludeAllFiles">Include all the files needed</a> in our Wise Standard)​​.<br></p><dl class="image"><dt><img src="HelpRunUnitTests.gif" alt="HelpRunUnitTests.gif" /></dt><dd>Figure: Standard Help menu should give you an option to Run Unit Tests to check the users' environment (Good)</dd></dl><dl class="image"><dt><img src="NUnitGui.gif" alt="NUnitGui.gif" /></dt><dd>Figure: Obviously the red indicates that there is a problem with a Unit Test (Good)<br></dd></dl>
<p>We have a rule <a href="/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&TermId=d15a7db4-1420-45c1-bdd2-21e92ec2c0a9">Do you know the Seven items every Help menu needs?</a>​​<br><br></p>


