---
type: rule
title: Do you use the best Code Analysis tools?
uri: do-you-use-the-best-code-analysis-tools
created: 2012-03-16T08:43:44.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 23
  title: Damian Brady
- id: 3
  title: Eric Phan

---

 ​​Whenever you are writing code, you should always make sure it conforms to your team's standards. The more pain a developer has when trying to check in, the better, because there will be less left up to testers to find.​



​​No matter how good a coder you are, you will always miss some of them some of the time, so it's a really good idea to have a tool that automatically scans your code and reports on what you need to change in order to improve it.​





Visual Studio has a great Code Analysis tool to help you look for problems in your code. Combine this with Jetbrain's ReSharper and your code will be smell free.​

The levels of protection are:

​​​![CricketHelmet.jpg](/SoftwareDevelopment/RulestobetterArchitectureandCodeReview/PublishingImages/CricketHelmet.jpg)

Figure: You wouldn't play cricket without protective gear and you shouldn't code without protective tools​



### Level 1

Get ReSharper to green on each file you touch. You want the files you work on to be left better than when you started. See [Do you follow the boyscout rule?](http&#58;//www.ssw.com.au/ssw/standards/rules/RulestoBetterCode.aspx#BoyscoutRule)

**Tip**: You can run through a file and tidy it very quickly if you know two great keyboard shortcuts:

- Alt + [Page Down/Page Up] : Next/Previous Resharper Error / Warning
- Alt + Enter: Smart refactoring suggestions

![Image 01](/SoftwareDevelopment/RulestobetterArchitectureandCodeReview/PublishingImages/image001.png)
​Figure: ReSharper will show Orange when it detects that there is code that could be improved![image002.png](/SoftwareDevelopment/RulestobetterArchitectureandCodeReview/PublishingImages/image002.png)​Figure: ReSharper will show green when all code is tidy
### Level 2

Run Code Analysis (was FxCop) with the default settings
![runcodeanalysisvs11.png](/SoftwareDevelopment/RulestobetterArchitectureandCodeReview/PublishingImages/CodeAnalysisVS11.png)Figure: Run Code Analysis in VS2012


![Code Analysis](/SoftwareDevelopment/RulestobetterArchitectureandCodeReview/PublishingImages/codeanalysis.png)Figure: The Code Analysis results indicate there are 17 items that need fixing
### Level 3

Ratchet up your Code Analysis Rules until you get to 'Microsoft All Rules'
![image003.png](/SoftwareDevelopment/RulestobetterArchitectureandCodeReview/PublishingImages/image003.png)Figure: Start with the Minimum Recommended Rules, and then ratched up.
### Level 4

Is to use StyleCop to check that your code has consistent style and formatting.
![stylecop.png](/SoftwareDevelopment/RulestobetterArchitectureandCodeReview/PublishingImages/StyleCopInVS2010.png)Figure: StyleCop shows a lot of warnings in this test project
### Level 5

Is to use [Code Auditor.](http&#58;//www.ssw.com.au/ssw/CodeAuditor/Default.aspx)

**Note:** Document any rules you've turned off.

### Level 6

Is to document any rules you've turned off.

All of these rules allow you to disable rules that you're not concerned about.  There's nothing wrong with disabling rules you don't want checked, but you should make it clear to developers why those rules were removed.

Create an **\_InstructionsCodeAnalysis.doc **document in your solution with the rules that have been turned off and why.

More Information: [Do you make instructions at the beginning of a project and improve them gradually?​​](/SoftwareDevelopment/RulesToBetterDotNETProjects/Pages/DoYouMakeInstructions.aspx)
![stylecop_removed_rules.png](/SoftwareDevelopment/RulestobetterArchitectureandCodeReview/PublishingImages/StyleCopRemovedRules.png)Figure: The document \_InstructionsCodeAnalysis.doc shows that there were 3 StyleCop rules disabled.

Suggestion to MS: Allow developers to put a comment against any disabled rule when you turn it off
<br>TODO - Damian: Add image

​​​


See [Do you add SSW Code Auditor, NUnit and Microsoft FxCop project files to your Solution?](/SoftwareDevelopment/RulesToBetterDotNETProjects/Pages/AddCAFxCopToSolution.aspx)

See [Do you check your code by Code Auditor before check-in?](/Management/RulesToSuccessfulProjects/Pages/CheckCodeByCodeAuditorBeforeCheckIn.aspx)


