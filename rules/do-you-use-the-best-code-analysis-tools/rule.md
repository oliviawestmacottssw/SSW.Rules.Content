---
type: rule
archivedreason: 
title: Do you use the best Code Analysis tools?
guid: 48fb228d-a09e-4c52-9c6a-eddfff34f08f
uri: do-you-use-the-best-code-analysis-tools
created: 2012-03-16T08:43:44.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
- title: Damian Brady
  url: https://ssw.com.au/people/damian-brady
- title: Eric Phan
  url: https://ssw.com.au/people/eric-phan
related: []
redirects: []

---

Whenever you are writing code, you should always make sure it conforms to your team's standards. If everyone is following the same set of rules; someone else’s code will look more familiar and more like your code - ultimately easier to work with.

No matter how good a coder you are, you will always miss things from time to time, so it's a really good idea to have a tool that automatically scans your code and reports on what you need to change in order to improve it.

Visual Studio has a great Code Analysis tool to help you look for problems in your code. Combine this with Jetbrains' ReSharper and your code will be smell free.

The levels of protection are:

<!--endintro-->
<dl class="image"><dt> 
      <img alt="CricketHelmet.jpg" src="CricketHelmet.jpg"> 
      <br> 
   </dt><dd>Figure: You wouldn't play cricket without protective gear and you shouldn't code without protective tools </dd></dl>
### Level 1

Get ReSharper to green on each file you touch. You want the files you work on to be left better than when you started. See     [Do you follow the boyscout rule?](http://www.ssw.com.au/ssw/standards/rules/RulestoBetterCode.aspx#BoyscoutRule)

**Tip:** You can run through a file and tidy it very quickly if you know two great keyboard shortcuts:

* Alt + [Page Down/Page Up] : Next/Previous Resharper Error / Warning
* Alt + Enter: Smart refactoring suggestions

<dl class="image"><dt> 
      <img alt="Image 01" src="48bc81_image001.png" style="width:750px;"> 
   </dt><dd> Figure: ReSharper will show Orange when it detects that there is code that could be improved</dd></dl><dl class="image"><dt> 
      <img alt="image002.png" src="image002.png" style="width:750px;"> 
   </dt><dd> Figure: ReSharper will show green when all code is tidy</dd></dl>
### Level 2

Is to use     [Code Auditor.](http://www.ssw.com.au/ssw/CodeAuditor/Default.aspx)
<dl class="image"><dt> 
      <img class="ms-rteCustom-ImageArea" alt="stylecop.png" src="CodeAuditor.png" style="width:750px;"> 
   </dt><dd>Figure: Code Auditor shows a lot of warnings in this test project</dd></dl>
**Note:** Document any rules you've turned off.

### Level 3

Is to use     [Link Auditor](http://www.ssw.com.au/ssw/LinkAuditor/).

**Note:** Document any rules you've turned off.

### Level 4

Is to use StyleCop to check that your code has consistent style and formatting.
<dl class="image"><dt> 
      <img alt="stylecop.png" src="StyleCopInVS2010.png" style="width:750px;"> 
   </dt><dd>Figure: StyleCop shows a lot of warnings in this test project</dd></dl>
### Level 5

Run Code Analysis (was FxCop) with the default settings or ReSharper with Code Analysis turned on
<dl class="image"><dt> 
      <img alt="runcodeanalysisvs11.png" src="CodeAnalysisVS11.png"> 
   </dt><dd>Figure: Run Code Analysis in Visual Studio<br></dd></dl><dl class="image"><dt> 
      <img alt="Code Analysis" src="codeanalysis.png"> 
   </dt><dd>Figure: The Code Analysis results indicate there are 17 items that need fixing</dd></dl>
### Level 6

Ratchet up your Code Analysis Rules until you get to 'Microsoft All Rules'
<dl class="image"><dt> 
      <img alt="image003.png" src="image003.png"> 
   </dt><dd>Figure: Start with the Minimum Recommended Rules, and then ratched up.</dd></dl>
### Level 7

Is to document any rules you've turned off.

All of these rules allow you to disable rules that you're not concerned about.  There's nothing wrong with disabling rules you don't want checked, but you should make it clear to developers why those rules were removed.

Create a      **GlobalSuppressions.cs** file in your project with the rules that have been turned off and why.
<dl class="image"><dt><img src="suppressions-file.png" alt="suppressions-file.png" style="width:750px;"></dt><dd>Figure: The suppressions file tells Code Analysis which rules it should disable for specific code blocks</dd></dl>
**More Information:** [Do you make instructions at the beginning of a project and improve them gradually?](/do-you-make-instructions-at-the-beginning-of-a-project-and-improve-them-gradually) and     https://docs.microsoft.com/en-us/visualstudio/code-quality/in-source-suppression-overview

### Level 8

The gold standard is to use <br>   [SonarQube](https://www.sonarqube.org/), which gives you the code analysis that the previous levels give you as wells as the ability to analyze technical debt and to see which code changes had the most impact to technical debt
<dl class="image"><dt> 
      <img src="2016-06-08_12-59-38.png" alt="2016-06-08_12-59-38.png" style="width:750px;"> 
   </dt><dd> Figure:  SonarQube workflow with Visual Studio and Azure DevOps<br></dd></dl><dl class="image"><dt> 
      <img src="2016-06-08_12-59-53.png" alt="2016-06-08_12-59-53.png">  
   </dt><dd> Figure: SonarQube gives you the changes in code analysis results between each check-in<br><br><br></dd></dl>
