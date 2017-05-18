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

 
​

One of the annoying things with SharePoint document libraries is that users often accidentally leave checked out files, that preventing others from modifying them.​​

Suggestion to Microsoft: send an email to the user to remind them they have outstanding checkouts potentially blocking other users.
![sp-docs.jpg](/PublishingImages/sp-docs.jpg)Figure: Here Eric Phan has not checked in a file 


**Upgrade warning:** The pages that are not checked-in, will not be migrated on a SharePoint upgrade. There is \*no\* warning either.​

There are 2 ways to remind users of their "checked out files":​

- **Solution A: Manage Content and Structure Report (No Code)​**
- **Solution B: Custom application report (Includes some coding work)​
Eg. SSW.SharePoint.CheckedOutFilesReport​
**

   ​  
**Solution A. Manage Content and Structure Report (No Code)**

1. Create CAML query in site content and structure

Go to "Site Settings | Manage Content and Structure | Content and Structure Reports", click "New":
![ContentAndStructureReportsNew.png](/PublishingImages/ContentAndStructureReportsNew.png)Figure: Create a new report
Fill the "CAML Query":
&lt;Where&gt;&lt;IsNotNull&gt;&lt;FieldRef Name="CheckoutUser" LookupId="TRUE"/&gt;&lt;/IsNotNull&gt;&lt;/Where&gt;

Fill the other fields like below:
![NewReportForm.png](/PublishingImages/NewReportForm.png)Figure: Fill in form
2. Run Checked Out report

 

Run the checkout report from "Site Settings | Manage Content and Structure | View: Checked out documents":
![CheckedOutDocuments.png](/PublishingImages/CheckedOutDocuments.png)Figure: Checked Out Documents report link Make sure there are no files checked out, otherwise, go step 3
3. Go chase after the users.
​ <br>   
**Solution B. Custom application report (Includes some coding work)
**


**TODO: **Move this tool to GitHub, find a better name than "SSW.SharePoint.CheckedOutFilesReport".  Also change from a farm solution to a solution that can be used on Office365 - now in SharePoint 2016 and SharePoint online called "Sharepoint Add-ins" 


To make reminding users easier, this SharePoint Add-in ha​s a custom page to show the "Checked out files". One button will send the notification email to all the naughty people. 



Even better, we have also improved the application with a scheduled task using SharePoint CSOM API to find checked out files and send these notification emails automatically​ every night.


![CheckedOutFilesApplicationReport.png](/PublishingImages/CheckedOutFilesApplicationReport.png)Figure: One button reminds all users of their "Checked out Files"



**Hi Daragh, **

 

You have some pages checked out in SharePoint.


> 1. Revise our SSW rule <br>            [on Frequent SharePoint Check-ins](/Pages/DoYouConfirmThereIsNoCheckedOutData.aspx).
> 2. If you are no longer editing these files, check them in!


 





You currently have the following pages checked out:


> • <br>            [http://&lt;siteurl&gt;/DesignandPresentation/RulesToBetterVideoRecording/Pages/Default.aspx](/Pages/DoYouConfirmThereIsNoCheckedOutData.aspx)
> • <br>            [http://&lt;siteurl&gt;/DesignandPresentation/RulesToBetterVideoRecording/Pages/testing-rule.aspx](/Pages/DoYouConfirmThereIsNoCheckedOutData.aspx)



Remember, you can check which files you have checked out at any time by going to <br>         [http://&lt;siteurl&gt;/\_layouts/SSWReports/CheckedOutReport.aspx](/Pages/DoYouConfirmThereIsNoCheckedOutData.aspx)


&lt;As per rule <br>         [http://rules.ssw.com.au/ITAndNetworking/SharePoint/Pages/DoYouConfirmThereIsNoCheckedOutData.aspx](/Pages/DoYouConfirmThereIsNoCheckedOutData.aspx) &gt;




​--Powered by SSW.SharePoint.CheckedOutFilesReport

 Figure: An example of the reminder email that all users receive 



