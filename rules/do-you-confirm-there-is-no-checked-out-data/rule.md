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

![ContentAndStructureReportsNew.png](/PublishingImages/ContentAndStructureReportsNew.png) 
Figure: Create a new report 
Fill the "CAML Query": 
&lt;Where&gt;&lt;IsNotNull&gt;&lt;FieldRef Name="CheckoutUser" LookupId="TRUE"/&gt;&lt;/IsNotNull&gt;&lt;/Where&gt;

 


Fill the other fields like below:

![NewReportForm.png](/PublishingImages/NewReportForm.png) 

Figure: Fill in form



2. Run Checked Out report

 

Run the checkout report from "Site Settings | Manage Content and Structure | View: Checked out documents":

![CheckedOutDocuments.png](/PublishingImages/CheckedOutDocuments.png)

Figure: Checked Out Documents report link make sure there are no files checked out, otherwise, go step 3. 

3. Go chase after the users.




**B. Custom application report (Includes some coding work)**
In SSW, to make the chase work easier, we have a custom page to show the "Checked out files" and send the notification email to naughty people:

![CheckedOutFilesApplicationReport.png](/PublishingImages/CheckedOutFilesApplicationReport.png) 

Figure: "Checked out Files" custom application report

 

Notification email sample: 


**Hi Daragh, **

 

You have some pages checked out in SharePoint. 


> 1. Revise our SSW rule [on Frequent SharePoint Check-ins](/Pages/DoYouConfirmThereIsNoCheckedOutData.aspx).
> 2. If you are no longer editing these files, check them in!


 





You currently have the following pages checked out: 


> • [http://&lt;siteurl&gt;/DesignandPresentation/RulesToBetterVideoRecording/Pages/Default.aspx](/Pages/DoYouConfirmThereIsNoCheckedOutData.aspx)
> • [http://&lt;siteurl&gt;/DesignandPresentation/RulesToBetterVideoRecording/Pages/testing-rule.aspx](/Pages/DoYouConfirmThereIsNoCheckedOutData.aspx)



Remember, you can check which files you have checked out at any time by going to [http://&lt;siteurl&gt;/\_layouts/SSWReports/CheckedOutReport.aspx](/Pages/DoYouConfirmThereIsNoCheckedOutData.aspx)


&lt;As per rule [http://rules.ssw.com.au/ITAndNetworking/SharePoint/Pages/DoYouConfirmThereIsNoCheckedOutData.aspx](/Pages/DoYouConfirmThereIsNoCheckedOutData.aspx) &gt;

William




