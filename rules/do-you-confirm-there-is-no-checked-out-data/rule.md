---
type: rule
title: Do you confirm there is no checked out data?
uri: do-you-confirm-there-is-no-checked-out-data
created: 2012-05-31T03:08:59.0000000Z
authors:
- id: 70
  title: Greg Harris
- id: 1
  title: Adam Cogan
- id: 9
  title: William Yin

---

 
Pages in SharePoint are easily checked out, and the changes not checked-in will not be migrated when you do migration for SharePoint data.

In SSW, we have two ways to check the "checked out files" regularly:

- **A. Manage Content and Structure Report (No Code)**
- **B. Custom application report (Includes some coding work)**

   ​ 
**A. Manage Content and Structure Report (No Code)**

1. Create CAML query in site content and structure

Go to "Site Settings | Manage Content and Structure | Content and Structure Reports", click "New":

![ContentAndStructureReportsNew.png](/ITAndNetworking/SharePointMigration/PublishingImages/ContentAndStructureReportsNew.png)
Figure: Create a new report 
Fill the "CAML Query": 
&lt;Where&gt;&lt;IsNotNull&gt;&lt;FieldRef Name="CheckoutUser" LookupId="TRUE"/&gt;&lt;/IsNotNull&gt;&lt;/Where&gt;

 


Fill the other fields like below:

![NewReportForm.png](/ITAndNetworking/SharePointMigration/PublishingImages/NewReportForm.png)

Figure: Fill in form



2. Run Checked Out report

 

Run the checkout report from "Site Settings | Manage Content and Structure | View: Checked out documents":

![CheckedOutDocuments.png](/ITAndNetworking/SharePointMigration/PublishingImages/CheckedOutDocuments.png)

Figure: Checked Out Documents report link make sure there are no files checked out, otherwise, go step 3. 

3. Go chase after the users.




**B. Custom application report (Includes some coding work)**
In SSW, to make the chase work easier, we have a custom page to show the "Checked out files" and send the notification email to naughty people:

![CheckedOutFilesApplicationReport.png](/ITAndNetworking/SharePointMigration/PublishingImages/CheckedOutFilesApplicationReport.png)
Figure: Checked out Files custom application report
