---
type: rule
title: Do you make instructions at the beginning of a project and improve them gradually?
uri: do-you-make-instructions-at-the-beginning-of-a-project-and-improve-them-gradually
created: 2009-05-13T06:12:34.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 17
  title: Ryan Tee
- id: 24
  title: Adam Stephensen

---

 ​​​​​​Instructions are very important when maintaining a project. With this document, people new to it can take over it quickly.
 


​There are 4 Levels of this documentation in a project.
​
Level 1 - Lots of documentation step by step​​

Add a document as a solution item and name it '\_Instru​​ctions.docx'

​​Tip: Microsoft Word documents are preferred over .txt files because images and formatting are important

You can also break up this document into 4 smaller documents

- \_Business.docx - Explaining the business purpose of the app
- \_Instructions\_Compile.docx - Contains instructions on how to get the project to compile
- \_Instructions\_Deployment.docx - Describes the deployment process
- \_Technologies.docx - Explaining the technical overview e.g. Broad architecture decisions, 3rd party utilities, patterns followed etc


Here's a suggestion of what these documents could contain.

1. Project structure <br>          All parts that composes the project and how they work with each other.
2. Third party components <br>          Any software, tools and DLL files that this project uses. (e.g., NHibernate, ComponentArt, KendoUI)
3. Database configuration
4. Other configuration information
5. Deployment information and procedures <br>
6. Other things to take care of

![A project with an instructions](/PublishingImages/BadNetProject.JPG)Bad example - A project without an instructions. ![Good Solutions Have Instructions](/PublishingImages/ProjectDocumentation.jpg)Good example - A project with instruction 
Level  1a:

VSTS with Markdown
Add a readme.md to your solution (Use [this​](https&#58;//docs.microsoft.com/en-us/azure/devops/project/wiki/markdown-guidance?view=vsts) as a guidance for markdown)​

## Level 2: Can you get latest and compile with a Docx

When a new developer starts on a project you want them to get up and running as soon as possible.

Problems to check for:

- Windows 8 not supported
- Many things to build
- Lots of dependencies


It is essential to have documentation that describes what is required to configure a developer workstation.
You are at Level 2 when you have the static word documents with the step to compile. The \_instructions\_compile.docx contains the steps required to be able to get latest and compile
## Level 3: Can you get latest and compile with the database
![Good Solutions Have Instructions - level 2](/PublishingImages/instructions-level2.jpg)Figure: Level 2 Documentation includes database build scripts. We use <br>      [SSW SQL Deploy](http&#58;//sqldeploy.com/) to make keeping all databases on the same version simple. Check out <br>      [how to use SQL Deploy here](http&#58;//tv.ssw.com/969/adam-stephensen-sql-deploy-demo)
## Level 4: Can you get latest and compile with a PowerShell script

A perfect solution would need no static documentation. Perfect code would be so self-explanatory that it did not need comments. The same rule applies with instructions on how to get the solution compiling: the best answer would be for the solution to contain scripts that automate the setup.


## Example of Level 4: PowerShell Documentation


**Recommendation:** All manual workstation setup steps should be scripted with powerShell (as per the below example)

**Recommendation:** You should be able to get latest and compile within 1 minute. Also, a developer machine should not HAVE to be on the domain (to support external consultants)

PS C:\Code\Northwind&gt;** .\Setup-Environment.ps1**

Problem: Azure environment variable run state directory is not configured (\_CSRUN\_STATE\_DIRECTORY).
 
Problem: Azure Storage Service is not running. Launch the development fabric by starting the solution.
 
WARNING: Abandoning remainder of script due to critical failures.
 
To try and automatically resolve the problems found, re-run the script with a -Fix flag.

Figure: Good example - you see the problems in the devs environment


PS C:\Code\Northwind&gt; .\Setup-Environment.ps1 -fix

Problem: Azure environment variable run state directory is not configured (\_CSRUN\_STATE\_DIRECTORY).

Fixed: \_CSRUN\_STATE\_DIRECTORY user variable set
 
Problem: Azure Storage Service is not running. Launch the development fabric by starting the solution.

WARNING: No automated fix availab ​​le for 'Azure Storage Service is running'
 
WARNING: Abandoning remainder of script due to critical failures.

Figure: Good example - when running with -fix this script tries to automatically fix the problem <br>      



PS C:\Code\Northwind&gt; .\Setup-Environment.ps1 -fix

Problem: Azure Storage Service is not running. Launch the development fabric by starting the solution.
WARNING: No automated fix available for 'Azure Storage Service is running'

WARNING: Abandoning remainder of script due to critical failures.



Figure: Good example -  Note that on the 2nd run, issues resolved by the 1st run are not re-reported <br>      


## Further Reading

To see other documentation Rules, have a look at     [Do you review the documentation?](/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=951ffbf9-4066-42f3-a9b7-e0d8603e728b)

