---
type: rule
title: Do you know how to handover a project?
uri: do-you-know-how-to-handover-a-project
created: 2010-03-15T06:22:03.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 13
  title: Paul Neumeyer

---

 A common source of pain, is picking up a project without a decent/complete handover. To have a successful project you must navigate over the problem of changing resources/people leaving etc.

<br>Always ensure that you complete the following checklist and *always*send the email confirming the handover is complete. 

<br>Here are the 7 steps you should follow for a good handover.     <br> 
1. Confirm current tasks
2. Confirm future tasks
3. Confirm the primary contacts
4. Do a code review
5. Review the client portal
6. Confirm location of info and procedures (hopefully these are on a wiki or SharePoint document library)
    - Source control
    - Documents
    - Deployment Steps
    - Servers and Passwords
    - Failure & Recovery Steps
7. Complete Handover by sending an email with: As per our meeting the handover has been completed to my satisfaction


**From: Andy
<br>To: Gracia
<br>Subject: SSW - Northwind handover**

Done

- **Confirm outstanding tasks **    Nothing.
- **Confirm planned tasks **    Get release 43 out.
- **Confirm location **
    - Source control<br>                Nothing
    - Data storage<br>                file://server/DataSSW/SSWProducts/Northwind
    - Deployment<br>                Make a build by using WISE
         Test: seadragon
         Production: squirrel
    - Failure & Recovery<br>                Do not work on the Master folder, work on local machine. If it has some issue, grab the file from master folder.
         Always backup master folder’s file before uploading the changes to the master folder
- **Update the Employee Responsibilities in SSW intranet **    **TODO**

**Figure Bad Example - This handover is incomplete and light on details** 


**From: Andy
<br>To: Gracia
<br>Subject: SSW - Northwind Handover**

DONE - As per our meeting the handover has been completed to my satisfaction



- **Confirm outstanding tasks **    Nothing.
- **Confirm planned tasks **    Next release is Release 43.
     The aim of this release is to improve the reporting available from the management module with chart reports
     Query = tfs\Northwind\Work Items\Team Queries\All Work Items - R43 - Management Module Reporting
    Backlog is in TFS.
     Query = tfs\Northwind\Work Items\Team Queries\All Work Items - Backlog
- **Confirm location **
    - Source control<br>                file://tfs.ssw.com.au/tfs/Northwind
    - Data storage<br>                file://server/DataSSW/SSWProducts/Norwind
    - Deployment
        - Make a build by using WISE
        - Test db to connect to:<br>                        server: seadragon
             database: SSWNorthwind\_test
        - Production db to connect to:<br>                        server: squirrel
             database: SSWNorthwind
    - Failure & Recovery<br>                Do not work on the Master folder, work on local machine. If it has some issue, grab the file from master folder.
         Always backup master folder’s file before uploading the changes to the master folder.
         If a problem occurs restore the backup of the master folder and restart
- **Update the Employee Responsibilities in SSW intranet **    DONE
- **Complete Handover **

**Figure: Good Example - This handover has lots of URLs and is complete**

If you need to handover only a single task there are more details here:
[http://sharepoint.ssw.com.au/Standards/Communication/RulesToBetterEmail/Pages/HandOverTask.aspx](/Standards/Communication/RulesToBetterEmail/Pages/HandOverTask.aspx)

