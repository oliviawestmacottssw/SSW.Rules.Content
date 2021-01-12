---
type: rule
archivedreason: 
title: Do you have a server reboot/restart policy?
guid: eb97dfa8-5bb8-4e19-932a-76d6f2f655fd
uri: do-you-have-a-server-reboot-restart-policy
created: 2017-06-30T19:21:55.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
- title: Stanley Sidik
  url: https://ssw.com.au/people/stanley-sidik
- title: Steven Andrews
  url: https://ssw.com.au/people/steven-andrews
related: []
redirects:
- have-a-server-reboot-restart-policy

---

For unplanned outages see: [https://rules.ssw.com.au/unplanned-outage-process](/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&TermId=d3f1bdc6-5ea1-495b-8c0d-98504963b563)

If your servers are down or have to go down during business hours you should notify the users at least 15 minutes beforehand so you will not get 101 people all asking you if the computer is down.

For short outages (under 15 minutes) that only affect only a few people (under 5 people), or are outside of business hours, then IM is the best method. If you use     [Teams or Skype](/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&TermId=3a474efa-ca72-4320-af36-b0e6af355684) a quick message will do.

**Note:** If they are not online on Teams or Skype, then they can't complain that they were not warned.

For extended or planned outages, or if you have a larger number of users (50+),      **email** is the suggested method.

<!--endintro-->

### Email

If you send an email it is a good idea to tell the user a way to monitor the network themselves. Eg. Software solutions like SCOM or WhatsUp Gold.

Include a "[To myself](/dones-do-you-send-yourself-emails)". It gives visibility to others who are interested in what needs to be done to fix the problem and makes
it easier to remember to send the 'done' email. E.g. "done - CRM is alive again".

Example:
 **To:** SSWALL


&gt;[What is your server reboot/restart policy?](/have-a-server-reboot-restart-policy)&lt;This is as per rule **Note:** 

1)	Restore server from backup
 **Backout Plan:** 
4)	Get result of user “Test Please” by email by 11:15 PM
3)	Call test users to start “Test Please” on the affect services
2)	Check each affected service is running
1)	Check Event log for errors
 **Test Plan:** **
** 7) Procedure completed
6) Based on result of test plan, follow backout plan if procedure failed
5) Follow test plan
4) Reboot server
3) Install Windows Updates
2)	Backup server
1)	Lockout users via IIS
 **Detailed Change Plan:** 
To show others who are interested in what needs to be done to fix the problem: **To myself,** 

**Note:** The following servers will be affected

![rule-outage-2.jpg](rule-outage-2.jpg)

http://wug.ssw.com.au/
![rule-outage-1.jpg](rule-outage-1.jpg) **Figure: Clearly showing the potential risks

** Hi All,

| **Risk**  |
| --- |
| | **Probability** |
| **Low** | **Medium** | **High** | **Unknown** |
| **Impact** | **Low** | Low risk | Low Risk | Low Risk | Medium Risk |
| **Medium** | Low Risk | Medium Risk | Medium Risk | High Risk |
| **High** | Medium Risk | High Risk | High Risk | High Risk |
| **Unknown** | Medium Risk <br>                  <br> | High Risk | High Risk | High Risk |


 **Risk Lookup Table by Probability and Impact:** 


| **Planned/Unplanned:**  | Planned |
| --- | --- |
| **Change Description:**  | Install Windows Updates and Restart Server<br> |
| **Risk (see table below):**  | LOW RISK (LOW Probability and MEDIUM Impact) |
| **Reason For Change:**  | Windows 2016 Windows Updates<br> |
| **Uptime over last month:**  | 91.361% |
| | <br> |
| **Planned Outage (mins):**  | 150 |
| **Planned Start Time:**  | 26 October 9:00 PM |
| **Planned Finish Time:**  | 26 October 11:30 PM<br> |
| |  |
| **Affected Services:**  | \\Windows Server 2016<br> |
| | http://sharepoint.ssw.com.au<br>http://intranet.ssw.com.au<br>http://projects.ssw.com.au |
| | <br> |



Here is the summary of the outage plan:



Immediately before the scheduled downtime, check for logged in users, file access, and database connections.

### Users

Open 'Windows Task Manager' (Run &gt; taskmgr) and select the 'Users' tab. Check with users if they have active connections, then have them log off.

::: ok  
![Figure: Connected users can be viewed in Task Manager](rule-outage-1.jpg)  
:::  

### Files

Open 'Computer Management' (Run &gt; compmgmt.msc), then 'System Tools &gt; Shared Folders'. Check 'Session' and 'Open Files' for user connections.

::: ok  
![Figure: Computer Management 'Open Files' View](rule-outage-1.jpg)  
:::  

### Database

Open SQL Server Management Studio on the server. Connect to the local SQL Server. Expand 'Management' and double-click 'Activity Manager'.

::: ok  
![Figure: SQL Management Studio 'Active Connections' View](rule-outage-1.jpg)  
:::  

Once these have been checked for active users, and users have logged off, maintenance can be carried out.

**Restarts should only be performed during the following time periods**

1. Between 7am and 7:05am
2. Between 1pm and 1:05pm
3. Between 7pm and 7:05pm <br>


If a scheduled shutdown is required, use the PsShutdown utility from [Microsoft's Sys Internals](https://www.ssw.com.au/ssw/Redirect/Microsoft/Technet.htm) page.

**Always reply 'Done' when you finish the task.**
