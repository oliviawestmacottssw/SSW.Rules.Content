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
3. In Excel, add a column called "Hours"​
Note: Once we move to estimating in time, this is no longer Scrum.
4. In Excel, copy this list and paste into another spreadsheet called the ![](/Style%20Library/SSW/CoreImages/iconXls.png "Excel File") [Estimates Calcul​ator](/Documents/4.%20Estimates%20Calculator.xlsx?d=w6f09d6a75d074fbda81e5e5dd3e18c76), in order to add all of the extra items (testing, DevOps, Project management, etc.).
Note: It would be great if TFS Web Access had functionality to add [standard items to a Release](http&#58;//www.ssw.com.au/ssw/Standards/BetterSoftwareSuggestions/TeamFoundationServer.aspx#StandardItems) (aka iteration)
5. Run a [test please](/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=d66a9404-2ca9-4d19-ad6c-df1618b4fc28) on this.
6. Add this spreadsheet to your specification review document.
7. When the Estimate is approved by the client, start work following these rules: [Rules to Better Project Management with TFS](http&#58;//www.ssw.com.au/ssw/Standards/Rules/RulesToBetterProjectManagementWithTFS.aspx).

 
**How to use the Estimates Calculator
**
Open the [Estimates Calculator](/Documents/4.%20Estimates%20Calculator.xlsx?d=w6f09d6a75d074fbda81e5e5dd3e18c76) and do the following:
![Resource tab.png](/PublishingImages/Resource%20tab.png)Figure: set the types and numbers of resources who will be working on the project

![Estimates tab.png](/PublishingImages/Estimates%20tab.png)Figure​: Enter your PBIs and estimates

Finally, you should copy and paste this estimates section into your proposal and present it to your client.




### Why Microsoft Project isn't recommended






- Tasks are auto scheduled based on dependency and resource allocation (who is assigned to it). This generates an estimated completion date which is never accurate, due to annual leave, public holidays and general shuffling of people in the team
- It gets the summing wrong (the totals don't seem to update and no way to trigger it)
- It's hard to synchronize with timesheets (as it doesn't connect to 3rd party timesheet systems out of the box – however, it does have its own time sheeting system, that is missing billing information!)
- You cannot allocate two people to a task. This create a lot of additional overhead to get it right. \*\*fixed in TFS 2008\*\*



