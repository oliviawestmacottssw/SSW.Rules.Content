---
type: rule
title: Do you have a consistent .NET Solution Structure?
uri: do-you-have-a-consistent-net-solution-structure
created: 2009-04-24T03:31:54.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 24
  title: Adam Stephensen

---

 
[SP Link](/Management/RulesToSuccessfulProjects/Pages/DoYouUnderstandTheValueOfConsistency.aspx)

[Web Link](/Management/RulesToSuccessfulProjects/Pages/DoYouUnderstandTheValueOfConsistency.aspx)

When developing a n-tiered software solution, we follow a standard solution structure. We have incorporated unit testing components, which is an integral part of the Extreme Programming development methodology, into our solution structure:
 

| Project Type  | Project Name  |  | Note  |
| --- | --- | --- | --- |
| Application  | Northwind  | <br><br>| **Namespace:**  | SSW.Northwind  |<br>| --- | --- |<br>| **Folder:**  | SSW\Northwind\Northwind\  |<br>| **Output:**  | Northwind.exe  |<br><br> |  |
| Class Library  | WindowsUI  | <br><br>| **Namespace:**  | SSW.Northwind.WindowsUI  |<br>| --- | --- |<br>| **Folder:**  | SSW\Northwind\WindowsUI\  |<br>| **Folder:**  | SSW\Northwind\WindowsUI.Tests  |<br>| **Output:**  | WindowsUI.dll  |<br><br> | We put all the forms in a separate project so we can run Unit Tests on the UI using reflection.Note if you have two projects you will give them different names (e.g. ProductSilverlightUI and AdminWebUI)  |
| Application  | ConsoleUI  | <br><br>| **Namespace:**  | SSW.Northwind.ConsoleUI  |<br>| --- | --- |<br>| **Folder:**  | SSW\Northwind\ConsoleUI\  |<br>| **Folder:**  | SSW\Northwind\ConsoleUI.Tests  |<br>| **Output:**  | NorthwindConsole.exe  |<br><br> |  |
| Application  | SilverlightUI  | <br><br>| **Namespace:**  | SSW.Northwind.SilverlightUI  |<br>| --- | --- |<br>| **Folder:**  | SSW\Northwind\SilverlightUI\  |<br>| **Folder:**  | SSW\Northwind\SilverlightUI.Tests  |<br>| **Output:**  | SSW.Northwind.SilverlightUI.dll  |<br><br> |  |
| Application  | WebUI  | <br><br>| **Namespace:**  | SSW.Northwind.WebUI  |<br>| --- | --- |<br>| **Folder:**  | SSW\Northwind\WebUI\  |<br>| **Folder:**  | SSW\Northwind\WebUI\UnitTests  |<br>| **Output:**  | SSW.Northwind.WebUI.dll  |<br><br> |  |
|  |  | <br><br>| **Namespace:**  | SSW.Northwind.WebUI.Reports  |<br>| --- | --- |<br>| **Folder:**  | SSW\Northwind\WebUI\Reports\  |<br><br> | Manually-based reports - e.g. using the DataGrid .<br><br>Part of WebUI. For .css and .ascx user controls |
| Windows Service  | WindowsService  | <br><br>| **Folder:**  | SSW\Northwind\WindowsService\Components  |<br>| --- | --- |<br>| **Folder:**  | SSW\Northwind\WindowsService.Tests  |<br>| **Output:**  | SSW.Northwind.WindowsService.dll  |<br><br> |  |
| RS Reports  | Reports  | <br><br>| **Namespace:**  | N/A  |<br>| --- | --- |<br>| **Folder:**  | SSW\Northwind\Reports  |<br>| **Output:**  | N/A  |<br><br> | Reporting Services<br><br>Note: We don't use Reports2005 or Reports2008 indicating the version number of reporting services because renaming in version control is a process intensive operation |
| Class Library  | IServices  | <br><br>| **Namespace:**  | SSW.Northwind.IServices  |<br>| --- | --- |<br>| **Folder:**  | SSW\Northwind\IServices  |<br>| **Folder:**  | SSW\Northwind\IServices.Tests  |<br>| **Output:**  | SSW.Northwind.IServices.dll  |<br><br> | WCF Services Interfaces<br><br>Note: only use if you are not hosting WCF in IIS |
| Class Library  | Services  | <br><br>| **Namespace:**  | SSW.Northwind.Services  |<br>| --- | --- |<br>| **Folder:**  | SSW\Northwind\Services  |<br>| **Folder:**  | SSW\Northwind\Services.Tests  |<br>| **Output:**  | SSW.Northwind.Services.dll  |<br><br> | WCF Services Implementations<br><br>Note: If you use WCF IIS Activation then you can put these under WebUI/Services to make deployment easier |
| Class Library  | Business  | <br><br>| **Namespace:**  | SSW.Northwind.Business  |<br>| --- | --- |<br>| **Folder:**  | SSW\Northwind\Business\  |<br>| **Folder:**  | SSW\Northwind\Business\Components  |<br>| **Folder:**  | SSW\Northwind\Business\UnitTests  |<br>| **Output:**  | SSW.Northwind.Business.dll  |<br><br> | This can be code-generated<br><br>(REPLACED BY SERVICES) |
| Class Library  | Domain  | <br><br>| **Namespace:**  | SSW.Northwind.Domain  |<br>| --- | --- |<br>| **Folder:**  | SSW\Northwind\Domain  |<br>| **Folder:**  | SSW\Northwind\Domain.Tests  |<br>| **Output:**  | SSW.Northwind.Domain.dll  |<br><br> | LINQ .EDMX AND .DBML sit here - this can be generated using SQL Metal (Replaces DataAccess and DataSets)<br><br>Note: LINQ to Entities is preferred over LINQ to SQL |
| Class Library  | DataSets  | <br><br>| **Namespace:**  | SSW.Northwind.DataSets  |<br>| --- | --- |<br>| **Folder:**  | SSW\Northwind\DataSets\  |<br>| **Folder: ** | SSW\Northwind\DataSets\UnitTests  |<br>| **Output:&gt;**  | SSW.Northwind.DataSets.dll  |<br><br> | Strongly typed datasets - this can be code-generated<br><br>(REPLACED BY DOMAIN) |
| Class Library  | DataAccess  | <br><br>| **Namespace:**  | SSW.Northwind.DataAccess  |<br>| --- | --- |<br>| **Folder:**  | SSW\Northwind\DataAccess\  |<br>| **Folder:**  | SSW\Northwind\DataAccess\Components  |<br>| **Folder:**  | SSW\Northwind\DataAccess\UnitTests  |<br>| **Output:**  | SSW.Northwind.DataAccess.dll  |<br><br> | This project should contain all the code and SQL statements used to access data from your backend. This project can be code-generated<br><br>(REPLACE BY DOMAIN) |
| Class Library  | Tests  | <br><br>| **Namespace:**  | SSW.Northwind.Domain.Tests  |<br>| --- | --- |<br>| **Folder:**  | SSW\Northwind.Domain.Tests\  |<br>| **Output:**  | SSW.Northwind.Domain.Tests.dll  |<br><br> | Only need this project if you are not using reusable components and then you do not need Tests folders above<br><br>For more information on [naming unit tests](http&#58;//www.ssw.com.au/SSW/Standards/rules/RulesToBetterUnitTests.aspx#OutsideProject) |
| Wise Setup  | Northwind  | <br><br>| **Folder:**  | SSW\Northwind\Setup\  |<br>| --- | --- |<br>| **Output:**  | SSWNorthwind\_v1-11.exe  |<br><br> | For Windows: Make an EXE in Wise instead of an MSI because it allows the application to be upgraded<br><br>For Web: Can be manual via an \_Instructions.doc or a Setup.bat file |


We have separated the unit tests, one for each project, for several reasons:

- It provides a clear separation of concerns and allows each component to be individually tested
- The different libraries can be used on other projects with confidence as there are a set of tests around them


For common library project, project name should include the company prefix and solution name, this is so other internal solution can include the common library's project. This will help debugging and development processes.


| Project Type  | Project Name  |  | Note  |
| --- | --- | --- | --- |
| Class Library  | Northwind.Common Business  | <br><br>| **Namespace:**  | Northwind.Common.Business  |<br>| --- | --- |<br>| **Folder:**  | ..\Northwind\Common\Business\  |<br>| **Output:**  | Northwind.Common.Business.dll  |<br><br> | No space in the Project Name  |


For project documents, we should also add them into solution for later reference, and different document types will be put in different folder, e.g. Mockup files will be in Northwind\Documents\Mockup\


| Project Type  | Project Name  |  | Note  |
| --- | --- | --- | --- |
| Documents  | Documents  | <br><br>| **Folder:**  | Northwind\Documents\  |<br>| --- | --- |<br><br> | This is outside the solution trunk  |

![solutionlayout.png](/SoftwareDevelopment/RulestobetterArchitectureandCodeReview/PublishingImages/SolutionLayout.png) Figure: Good Example - The Solution and Projects are named consistently
