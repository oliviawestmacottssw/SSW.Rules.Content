---
type: rule
archivedreason: This applies to old versions of Visual Studio as the test frameworks now provide their own test runner implementations for Visual Studio
title: Do you know how to run nUnit tests from within Visual Studio?
guid: a0ea3600-18d7-4384-b9b5-f991a0d6d214
uri: do-you-know-how-to-run-nunit-tests-from-within-visual-studio
created: 2020-03-12T22:45:00.0000000Z
authors:
- id: 1
  title: Adam Cogan
related: []
redirects: []

---

### Option 1: External tool (not recommended)


Using NUnit with Visual Studio: To make it easy to use, you need to add it as an external tool in Visual Studio.

In Visual Studio:

1. Go to Tools > External Tools
2. Click "Add" button
3. Type in:


* Title: NUnit GUI
* Command: Location of nUnit.exe file
* Argument: /run (so that the tests run automatically when started)
* Initial Directory: $(Target directory)


<!--endintro-->

[[badExample]]
| ![NUnit In Visual Studio](NUnitInVStudio.jpg)
### Option 2: Test Driven .net


TestDriven.net has better NUnit integration – from both code and Solution Explorer windows.

![Better way - Use TestDriven.Net - it has a 'Run Test](UseTestDriven.jpg)(s)' command for a single test (above) or...
![...you can right-click on a project and select 'Test With > NUnit' to bring up the GUI. It is certainly more convenient](GUIBringUpAction.jpg)
To run unit testing: Tools > NUnit GUI to launch NUnit and run the tests.

### Option 3: Other Tools


Other Visual Studio tools including Resharper and Coderush have their own integration with NUnit. If you’re already using one of these, installing TestDriven.net is unnecessary.
