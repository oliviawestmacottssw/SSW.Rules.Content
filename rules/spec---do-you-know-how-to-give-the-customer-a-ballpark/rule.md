---
type: rule
title: Spec - Do you know how to give the customer a ballpark?
uri: spec---do-you-know-how-to-give-the-customer-a-ballpark
created: 2009-11-04T08:35:51.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 4
  title: Ulysses Maclaren
- id: 2
  title: Cameron Shaw
- id: 5
  title: Justin King

---

 
**How do I create an Estimate? ****
**

1. Use an [Excel template calcul​ator](/Management/RulesToBetterProjectManagement/Documents/SSWPrioritiesEstimatesTemplate.xlsx) to enter all your work items specific to the release including the estimates on the particular work items (enter estimates in days)
2. Run a [test please](/Management/RulesToSuccessfulProjects/Pages/InternalTestPlease.aspx) on the Release
3. When the Release is approved by the client [create a Release Plan in TFS](http&#58;//www.ssw.com.au/ssw/Standards/Rules/RulesToBetterProjectManagementWithTFS.aspx) and publish the excel to SharePoint.

<br>We also set our SharePoint document library's default template to be this file to allow developers to find it easily. ​​​ 
NB: It would be great if TFS Web Access had functionality to add [standard items to a Release](http&#58;//www.ssw.com.au/ssw/Standards/BetterSoftwareSuggestions/TeamFoundationServer.aspx#StandardItems) (aka iteration)

**Why Microsoft Project isn't recommended**

- Tasks are auto scheduled based on dependency and resource allocation (who is assigned to it). This generates an estimated completion date which is never accurate, due to annual leave, public holidays and general shuffling of people in the team
- It gets the summing wrong (the totals don't seem to update and no way to trigger it)
- It's hard to synchronize with timesheets (as it doesn't connect to 3rd party timesheet systems out of the box – however, it does have its own time sheeting system, that is missing billing information!)
- You cannot allocate two people to a task. This create a lot of additional overhead to get it right. \*\*fixed in TFS 2008\*\*


**How to create a Release Plan
**
![](/Management/RulesToBetterProjectManagement/PublishingImages/SSWBallPark-SharePointTemplate.jpg) Figure: Use SharePoint Document Library Template for creating consistent ballpark![](/Management/RulesToBetterProjectManagement/PublishingImages/SSWBallPark-SharePointTemplate-Instructions.jpg) Figure: Read the instructions about how to use this template 

![](/Management/RulesToBetterProjectManagement/PublishingImages/SSWBallPark-SharePointTemplate-MenuCalc.jpg) Figure: Use Menu Calculator to understand the common estimates 

![](/Management/RulesToBetterProjectManagement/PublishingImages/SSWBallPark-SharePointTemplate-Resources.jpg) Figure: Use Resources sheet to assign resources 

![](/Management/RulesToBetterProjectManagement/PublishingImages/SSWBallPark-SharePointTemplate-Ballpark.jpg) Figure: Use the Release sheet to enter all the work items and calculate ballpark 
Finally, you should copy and paste this Release sheet into an email and send to your client. Before that, make sure you talk your client through it first. 

![](/Management/RulesToBetterProjectManagement/PublishingImages/SSWBallPark-SharePointTemplate-Email.jpg) Figure: Send the ballpark by Email     

**Winning the Project- Publish these Work Items to TFS**

1. Open Visual Studio
2. Create a new Project in Team Explorer


![](/Management/RulesToBetterProjectManagement/PublishingImages/CreateNewProjectInTE.jpg)

3.  Define new Iterations
![](/Management/RulesToBetterProjectManagement/PublishingImages/AreasAndIterations.jpg)
Figure: Accessing the Areas and Iterations menu from your project in Team Explorer
![](/Management/RulesToBetterProjectManagement/PublishingImages/NamedIterations.jpg)Figure: Add appropriate named iterations

              4. In SharePoint, open your Release Summary
         5. Create a new Worksheet in the same Workbook for your release plan. Rename  it to "TFS Work Items"
         6. From the "Team" ribbon tab, click "New List"
         7. Select the Team Project you Created
![](/Management/RulesToBetterProjectManagement/PublishingImages/TeamProjectYouCreate.jpg)

         8. Click "Input List". This will connect Excel to TFS, and allow you to enter Work Items to be published
![](/Management/RulesToBetterProjectManagement/PublishingImages/InputList.jpg)

    After you do this, it will generate a worksheet that looks like this:


    9. Click "Choose Columns", and make sure these columns are selected in the following order:
        a. ID (will be included automatically);
        b. Title
        c. Baseline Work
        d. Work  Item Type
![](/Management/RulesToBetterProjectManagement/PublishingImages/ChooseColumns.jpg)

![](/Management/RulesToBetterProjectManagement/PublishingImages/Columns.jpg)


    10. Copy the first four columns of the release summary onto a blank section of the TFS Work Items work sheet
![](/Management/RulesToBetterProjectManagement/PublishingImages/CopyColumnsToWorksheet.jpg)

    11. Delete the Resources and Hours per resource column
![](/Management/RulesToBetterProjectManagement/PublishingImages/DeleteRHColumn.jpg)

12. Cut the Task and Man Hours column and paste it into the input list. You MUST use “Paste-Special”, and select Values, otherwise you will get an error.

13. Set the "Work Item Type":
        a. Subheading/Categories are considered "Scenarios" in TFS
        b. Work Items are set as "Task"

14. Click the "Publish" button from the ribbon. 
![](/Management/RulesToBetterProjectManagement/PublishingImages/ClickPublish.jpg)


