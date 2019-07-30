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

 


Whenever you are writing code, you should always make sure it conforms to your team's standards. If everyone is following the same set of rules; someone else’s code will look more familiar and more like your code - ultimately easier to work with.

No matter how good a coder you are, you will always miss things from time to time, so it's a really good idea to have a tool that automatically scans your code and reports on what you need to change in order to improve it.

Visual Studio has a great Code Analysis tool to help you look for problems in your code. Combine this with Jetbrains' ReSharper and your code will be smell free.

The levels of protection are:
 ![CricketHelmet.jpg](/PublishingImages/CricketHelmet.jpg)
Figure: You wouldn't play cricket without protective gear and you shouldn't code without protective tools 
### Level 1

Get ReSharper to green on each file you touch. You want the files you work on to be left better than when you started. See     [Do you follow the boyscout rule?](http&#58;//www.ssw.com.au/ssw/standards/rules/RulestoBetterCode.aspx#BoyscoutRule)

**Tip:** You can run through a file and tidy it very quickly if you know two great keyboard shortcuts:

- Alt + [Page Down/Page Up] : Next/Previous Resharper Error / Warning
- Alt + Enter: Smart refactoring suggestions

![Image 01](/PublishingImages/48bc81_image001.png) Figure: ReSharper will show Orange when it detects that there is code that could be improved![image002.png](/PublishingImages/image002.png) Figure: ReSharper will show green when all code is tidy
### Level 2

Is to use     [Code Auditor.](http&#58;//www.ssw.com.au/ssw/CodeAuditor/Default.aspx)
![stylecop.png](/PublishingImages/CodeAuditor.png)Figure: Code Auditor shows a lot of warnings in this test project
**Note:** Document any rules you've turned off.

### Level 3

Is to use     [Link Auditor](http&#58;//www.ssw.com.au/ssw/LinkAuditor/).

**Note:** Document any rules you've turned off.

### Level 4

Is to use StyleCop to check that your code has consistent style and formatting.
![stylecop.png](/PublishingImages/StyleCopInVS2010.png)Figure: StyleCop shows a lot of warnings in this test project
### Level 5

Run Code Analysis (was FxCop) with the default settings or ReSharper with Code Analysis turned on
![runcodeanalysisvs11.png](/PublishingImages/CodeAnalysisVS11.png)Figure: Run Code Analysis in Visual Studio
![Code Analysis](/PublishingImages/codeanalysis.png)Figure: The Code Analysis results indicate there are 17 items that need fixing
### Level 6

Ratchet up your Code Analysis Rules until you get to 'Microsoft All Rules'
![image003.png](/PublishingImages/image003.png)Figure: Start with the Minimum Recommended Rules, and then ratched up.
### Level 7

Is to document any rules you've turned off.

All of these rules allow you to disable rules that you're not concerned about.  There's nothing wrong with disabling rules you don't want checked, but you should make it clear to developers why those rules were removed.

Create a     **GlobalSuppressions.cs** file in your project with the rules that have been turned off and why.
![suppressions-file.png](/PublishingImages/suppressions-file.png)Figure: The suppressions file tells Code Analysis which rules it should disable for specific code blocks
**More Information:** [Do you make instructions at the beginning of a project and improve them gradually?](/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=d6d34c31-ac6a-49a4-876a-f9d30e1ab78a) and     [https://docs.microsoft.com/en-us/visualstudio/code-quality/in-source-suppression-overview](https&#58;//docs.microsoft.com/en-us/visualstudio/code-quality/in-source-suppression-overview)
  
### Level 8

The gold standard is to use <br>   [SonarQube](https&#58;//www.sonarqube.org/), which gives you the code analysis that the previous levels give you as wells as the ability to analyze technical debt and to see which code changes had the most impact to technical debt
![2016-06-08_12-59-38.png](/SiteAssets/do-you-use-the-best-code-analysis-tools/2016-06-08_12-59-38.png) Figure:  SonarQube workflow with Visual Studio and Azure DevOps​
![2016-06-08_12-59-53.png](/SiteAssets/do-you-use-the-best-code-analysis-tools/2016-06-08_12-59-53.png) Figure: SonarQube gives you the changes in code analysis results between each check-in



