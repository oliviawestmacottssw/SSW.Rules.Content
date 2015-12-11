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

 
**How to create an Estimate For a Spec Review (Summary)****
**

This process can take up to a few days, so if you're just after a ballpark, use epics instead of PBIs (Product Backlog Items).

1. Usually using the browser, list all of the PBIs in TFS, sizing them with story points.
2. Using Visual Studio, export the list of PBIs and Story Points to Excel.
3. In Excel, add a colum called "Days"
Convert the story points to days by deciding on a scaling factor based on your team's velocity. (e.g. Days = Effort/5... assuming you get about 5 story points done per day). 
Note: Once we move to estimating in days, this is no longer Scrum.
4. In Excel, copy this list and paste into another spreadsheet called the ![](/Style%20Library/SSW/CoreImages/iconXls.png "Excel File") [Excel template calcul​ator](/Documents/zzSSWPrioritiesEstimatesTemplate-v1.xlsx) ![](/Style%20Library/SSW/CoreImages/IconNewWindow.png "This opens in a New Window"), in order to add all of the extra items (training, testing, Project management, etc.).
Note: It would be great if TFS Web Access had functionality to add [standard items to a Release](http&#58;//www.ssw.com.au/ssw/Standards/BetterSoftwareSuggestions/TeamFoundationServer.aspx#StandardItems) (aka iteration)
5. Run a [test please](/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=d66a9404-2ca9-4d19-ad6c-df1618b4fc28) on this.
6. Add this spreadsheet to your specification review document.
7. When the Estimate is approved by the client, start work following these rules: [Rules to Better Project Management with TFS](http&#58;//www.ssw.com.au/ssw/Standards/Rules/RulesToBetterProjectManagementWithTFS.aspx).

<br>TODO - Ask Eric - We also set our SharePoint document library's default template to be this file to allow developers to find it easily. ​​​ 
**Why Microsoft Project isn't recommended**

- Tasks are auto scheduled based on dependency and resource allocation (who is assigned to it). This generates an estimated completion date which is never accurate, due to annual leave, public holidays and general shuffling of people in the team
- It gets the summing wrong (the totals don't seem to update and no way to trigger it)
- It's hard to synchronize with timesheets (as it doesn't connect to 3rd party timesheet systems out of the box – however, it does have its own time sheeting system, that is missing billing information!)
- You cannot allocate two people to a task. This create a lot of additional overhead to get it right. \*\*fixed in TFS 2008\*\*




**How to create a Release Plan
**
![](/PublishingImages/SSWBallPark-SharePointTemplate.jpg) Figure: Use SharePoint Document Library Template for creating consistent ballpark![](/PublishingImages/SSWBallPark-SharePointTemplate-Instructions.jpg) Figure: Read the instructions about how to use this template 

![](/PublishingImages/SSWBallPark-SharePointTemplate-MenuCalc.jpg) Figure: Use Menu Calculator to understand the common estimates 

![](/PublishingImages/SSWBallPark-SharePointTemplate-Resources.jpg) Figure: Use Resources sheet to assign resources 

![](/PublishingImages/SSWBallPark-SharePointTemplate-Ballpark.jpg) Figure: Use the Release sheet to enter all the work items and calculate ballpark 
Finally, you should copy and paste this Release sheet into an email and send to your client. Before that, make sure you talk your client through it first. 

![](/PublishingImages/SSWBallPark-SharePointTemplate-Email.jpg) Figure: Send the ballpark by Email     

**Winning the Project- Publish these Work Items to TFS**

1. Open Visual Studio
2. Create a new Project in Team Explorer


![](/PublishingImages/CreateNewProjectInTE.jpg)

3.  Define new Iterations
![](/PublishingImages/AreasAndIterations.jpg)
Figure: Accessing the Areas and Iterations menu from your project in Team Explorer
![](/PublishingImages/NamedIterations.jpg)Figure: Add appropriate named iterations

     4. In SharePoint, open your Release Summary
     5. Create a new Worksheet in the same Workbook for your release plan. Rename  it to "TFS Work Items"
     6. From the "Team" ribbon tab, click "New List"
     7. Select the Team Project you Created
![](/PublishingImages/TeamProjectYouCreate.jpg)

    8. Click "Input List". This will connect Excel to TFS, and allow you to enter Work Items to be published
![](/PublishingImages/InputList.jpg)

    After you do this, it will generate a worksheet that looks like this:


    9. Click "Choose Columns", and make sure these columns are selected in the following order:
        a. ID (will be included automatically);
        b. Title
        c. Baseline Work
        d. Work  Item Type
![](/PublishingImages/ChooseColumns.jpg)

![](/PublishingImages/Columns.jpg)


    10. Copy the first four columns of the release summary onto a blank section of the TFS Work Items work sheet
![](/PublishingImages/CopyColumnsToWorksheet.jpg)

    11. Delete the Resources and Hours per resource column
![](/PublishingImages/DeleteRHColumn.jpg)

12. Cut the Task and Man Hours column and paste it into the input list. You MUST use “Paste-Special”, and select Values, otherwise you will get an error.

13. Set the "Work Item Type":
        a. Subheading/Categories are considered "Scenarios" in TFS
        b. Work Items are set as "Task"

14. Click the "Publish" button from the ribbon. 
![](/PublishingImages/ClickPublish.jpg)


