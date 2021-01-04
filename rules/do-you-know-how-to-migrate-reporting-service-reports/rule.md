---
type: rule
archivedreason: 
title: Do you know how to migrate reporting service reports
guid: 684f90fc-01c1-43e5-b864-d4f3efabbf76
uri: do-you-know-how-to-migrate-reporting-service-reports
created: 2016-10-12T08:35:33.0000000Z
authors:
- title: Moss Gu
  url: https://ssw.com.au/people/moss-gu
related: []
redirects: []

---

`youtube: https://www.youtube.com/embed/1knwXRIbVNw`
 
 **Figure: How to migrate SSRS reports from an old server to another
** 
Let's say you want to migrate SSRS reports from an old reporting service server (e.g., SQL Server 2008 R2) to a new one (e.g., SQL Server 2016). What involves?

There are three steps:

<!--endintro-->

###  Step 1: Find the reports that don't need to be migrated

* You need to install [SSW SQL Reporting Service Auditor](https://www.ssw.com.au/ssw/SQLReportingServicesAuditor/ "SSW SQL Reporting Service Auditor")both on the old and new servers. (You'll also need to run it on 3rd step)
* Find those reports are not-in-use, as per a rule: <br>      [Do you know which reports are being used?](/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&TermId=ed18874b-3724-4388-8411-45f27f63f909)
* Find creators of those reports, by clicking “Detail Views” in reports folder<br>      <dl class="image">&lt;dt&gt;
            <img src="detailsview.png" alt="detailsview.png" style="width:750px;">
         &lt;/dt&gt;<dd>Figure: Find reports creators by clicking "Details View" inside report folder</dd></dl>
* Send an email to report creater ask for permission to delete 
<dl class="image">&lt;dt&gt; 
            <img src="sent.png" alt="sent.png" style="width:750px;"> 
         &lt;/dt&gt;<dd> Figure:  Send an email to ask permission</dd></dl><dl class="image">&lt;dt&gt; 
            <img src="receive.png" alt="receive.png" style="width:750px;height:327px;"> 
         &lt;/dt&gt;<dd>Figure: Email received with permission to delete from creator</dd></dl>

### 2. Migrate those in-use reports from old server to new server


> Tip: use the           [ReportSync](https://github.com/dapaxx/reportsync) tool to save time


### 3. Check audit results
    * Run SSW SQL Reporting Service Auditor on both sides
    * Compare audit results. Note that even error and warning messages also need to be the same
    If audit results are exactly the same on old and new servers, it indicates that migration is successful.
