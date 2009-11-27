---
type: rule
title: Do you use MS Project to track project budget usage?
uri: do-you-use-ms-project-to-track-project-budget-usage
created: 2009-11-27T05:46:28.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 10
  title: Lei Xu

---

 As long as you have work items created and your developers keep them up to date, you can use MS Project to calculate project budget usage in real-time; this helps the project manager to determine the progress in term of $ which is what client really care about. 
<br>Note: To have this working properly, you need VSTS 2010 because it has better MS Project integration. 
**Calculate the total cost for your release:** 
 Follow the steps below to save a baseline and track your project budget usage:

1. Open MS Project and connect to your Team Project ![](/Standards/Management/RulesToBetterProjectManagement/PublishingImages/ChooseTeamProject_Small.jpg) Figure: Click “Choose Team Project” and choose the project you want to track
2. Query the work items from the team project ![](/Standards/Management/RulesToBetterProjectManagement/PublishingImages/QueryTheWorkItem_Small.jpg)Figure: Click on “Get Work Items” and choose query to select the work items you want to trackNote: normally you want to create queries for each of your Release, then you can quickly import them together.
3. To Track progress, we will want to use “Team System Task Sheet” view, you can choose this from “View” menu.
4. You will have your work items imported and they will be arranged with hierarchy, because we are trying to track the progress, we want to keep “Original Estimate”, “Remaining Work” and “Completed Work” together, so drag them after the Work Item Title. ![](/Standards/Management/RulesToBetterProjectManagement/PublishingImages/ArrangeWorkItems_Small.jpg)Figure: Arrange your work items so we can easily track their progress
5. To have the cost calculated, we need to assign rate for each of the resources. Go to “View, Resource Sheet”, then you can assign rate for your resources: 
![](/Standards/Management/RulesToBetterProjectManagement/PublishingImages/AssignResourceRates.jpg)Figure: Assign resources rates
6. When you switch back to “Team System Task Sheet”, you will want to add the following fields so we can see the cost status;
<br>      a.  Baseline Cost
<br>      b. Remaining Cost
<br>      c. Actual Cost 
<br>    You will notice the “Remaining Cost” column has been calculated based on the “Remaining Work” column and the Rate we entered for each task. 
![](/Standards/Management/RulesToBetterProjectManagement/PublishingImages/CostColumn_Small.jpg)Figure: Showing cost columns
7. However, this will not giving you a total cost for your current release. You can do this by adding a summary task on the top so MS Project will calculate that for you.
<br>    Choose the 1st task in your project, right click and create a “New Task” 
![](/Standards/Management/RulesToBetterProjectManagement/PublishingImages/SummaryTask.jpg)Figure: Create a summary task at the top Name the task as per your release name so you know what this plan is for; also you don’t want this task to be created in your TFS as a work item because it’s just a summary, set “Publish and Refresh” as “No”. 
![](/Standards/Management/RulesToBetterProjectManagement/PublishingImages/NoPublishAndRefresh.jpg)Figure: Don’t publish and refresh this summary task To make this as a summary, you need to select all the rest tasks and indent them by clicking the little red forward arrow in the tool bar.
![](/Standards/Management/RulesToBetterProjectManagement/PublishingImages/IndentTask_Small.jpg)Figure: Indent tasks Now, your summary task is ready and it’s showing the total cost for your current release: ![](/Standards/Management/RulesToBetterProjectManagement/PublishingImages/TotalCost_Small.jpg) Figure: Total cost is calculated


**Baseline management:**
 Baseline management is very important for every project managers as it helps you to determine the budget usage; the initial estimate of the project should be approved by the client, at this point it becomes your initial baseline. So before you set a baseline in your MS Project, make sure it’s approved by the client.

To set a baseline, choose “Tools, Tracking, Set Baseline” from the menu: ![](/Standards/Management/RulesToBetterProjectManagement/PublishingImages/SetBaseline_Small.jpg)Figure: Set Baseline …![](/Standards/Management/RulesToBetterProjectManagement/PublishingImages/ChooseBaseline.jpg)Figure: Choose “Baseline” and click ok

MS Project allows you to set multiple baselines; this is very handy because when the project is running, client will want to add/remove tasks from the project, then they will need to approve a new baseline. 
 Once your baseline is set, you will be able to see the “Baseline Cost” column is showing $,![](/Standards/Management/RulesToBetterProjectManagement/PublishingImages/BaselineCost_Small.jpg)Figure: Baseline Cost is showing $

**Track your project on the go**
 When your project is running, your developers will update the “Remaining Work” and “Completed Work” columns from TFS, they may not use MS Project so you will need to refresh your MS Project file to get these changes, and the $ will be calculated on the fly to give you up-to-date status.
![](/Standards/Management/RulesToBetterProjectManagement/PublishingImages/BudgetUsage_Small.jpg)Figure: Budget usage is calculated. Note: if the values are not calculated, it maybe your calculation mode is set to “manual”, then you need to hit F9 to force MS Project to calculate. Or you can change this setting in “Tools, Options, Calculation”. 
![](/Standards/Management/RulesToBetterProjectManagement/PublishingImages/CalculationMode_Small.jpg)Figure: set the calculation mode to “Automatic”Also make sure “Actual costs are always calculated by Microsoft Office Project” is enabled.

