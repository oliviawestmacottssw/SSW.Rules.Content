---
type: rule
title: Do you Add SSW Code Auditor, NUnit and Microsoft FxCop project files to your Solution
uri: do-you-add-ssw-code-auditor-nunit-and-microsoft-fxcop-project-files-to-your-solution
created: 2009-05-06T09:26:46.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 17
  title: Ryan Tee

---

[SSW Code Auditor](http&#58;//www.ssw.com.au/ssw/CodeAuditor/Default.aspx), [NUnit](http&#58;//www.ssw.com.au/ssw/Standards/DeveloperGeneral/netTools.aspx#NUnit) and [Microsoft FxCop](http&#58;//www.ssw.com.au/ssw/Standards/DeveloperGeneral/netTools.aspx#FxCop) are tools to keep your code "healthy". That is why they should be easily accessible in every solution so that they can be run with a double click of a mouse button. <br> 

![Code Auditor Project File](/Standards/SoftwareDevelopment/RulesToBetterDotNETProjects/PublishingImages/CodeAuditorProjectFile.gif) 
To add a [SSW Code Auditor](http&#58;//www.ssw.com.au/ssw/CodeAuditor/Default.aspx) file to your solution:

1. Start up SSW Code Auditor
2. Add a **new Job**
3. Add a the solution file to be scanned
4. Select the rules to be run
5. Configure email (not required)
6. Select **File &gt; Save As** (into the solution's folder as "c**odeauditor.SSWCodeAuditor**")
7. Open your Solution in Visual Studio
8. Right click and **add existing file**
9. Select the **SSW Code Auditor project file**
10. Right click the newly added file and select "**Open With**"
![Open With](/Standards/SoftwareDevelopment/RulesToBetterDotNETProjects/PublishingImages/OpenWith.gif)
11. Point it to the SSW Code Auditor executable


 See [Do you run SSW Code Auditor?](http&#58;//www.ssw.com.au/ssw/Standards/Rules/RulesToBeingSoftwareConsultantsWorkingInATeam.aspx#CodeAuditor) 
 See [Do you check your code by Code Auditor before check-in?](/Standards/Management/RulesToSuccessfulProjects/Pages/CheckCodeByCodeAuditorBeforeCheckIn.aspx) 
 To add a [Microsoft FxCop](http&#58;//www.ssw.com.au/ssw/Standards/DeveloperGeneral/netTools.aspx#FxCop)file to your solution:
1. Stat up **Microsoft FxCop**
2. Create a **New Project**
3. Right click the project and **Add Target**
4. Select the Assembly (DLL/EXE) for the project
5. Select **File &gt; Save Project As **(into the solution's folder as "**fxcop.FxCop**")
6. Open your Solution in Visual Studio
7. Right click and **add existing file**
8. Select the **Microsoft FxCop project file**
9. **Right click** the newly added file and select "**Open With**"
10. Point it to the Microsoft FxCop executable


 To add a [NUnit](http&#58;//www.ssw.com.au/ssw/Standards/DeveloperGeneral/netTools.aspx#NUnit)file to your solution:
1. Stat up **NUnit**
2. Create a New Project by selecting **File &gt; New Project** and save it to your solution directory as "**nunit.NUnit**"
3. From the **Project** menu select **Add Assembly**
4. Select the Assembly (DLL/EXE) for the project that contains unit tests
5. Select **File &gt; Save Project**
6. Open your Solution in Visual Studio
7. Right click and **add existing file**
8. Select the **NUnit project file**
9. **Right click** the newly added file and select "**Open With**"
10. Point it to the NUnit executable


Now you can simply double click these project files to run the corresponding applications.


| We have a program called [SSW Code Auditor](http&#58;//www.ssw.com.au/ssw/CodeAuditor/Default.aspx) that implements this rule. |
| --- |


