---
type: rule
archivedreason: 
title: Files - Do you know where to keep your files?
guid: 67e2605b-3b35-43b2-af8d-f17ee023af41
uri: files-do-you-know-where-to-keep-your-files
created: 2011-08-29T19:18:47.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
- title: Tiago Araujo
  url: https://ssw.com.au/people/tiago-araujo
- title: Liam Elliott
  url: https://ssw.com.au/people/liam-elliott
related: []
redirects:
- files---do-you-know-where-to-keep-your-files

---

Each client project should have a nice place to keep files. In the old days, things were simple but limited, we simply used Windows Explorer and file shares. Today there are so many places that teams can store documents. E.g Dropbox, OneDrive, SharePoint, Microsoft Teams and Azure DevOps (was TFS).
<dl class="image"><dt><img src="Screen Shot 2020-10-29 at 11.02.48 AM.png" alt="Too much email"><br></dt></dl>
<!--endintro-->

### Which is the best corporate solution?


The solution that allows the best collaboration with Developers, Project Managers, and other stakeholders is SharePoint and Microsoft Teams. It is super easy to create, upload, and share documents with others.
<dl class="image"><dt>
      <img src="Microsoft-Teams-Files.png" alt="Microsoft-Teams-Files.png" style="width:750px;">
   </dt><dd>Figure: Teams | Team | Files. More at 
      <a href="/the-best-place-to-store-documents-and-share-them">https://rules.ssw.com.au/track-project-documents</a><br></dd></dl>
### What emails do you need to store?

More at [Sales - Do you track all sales related activities in CRM?](/sales-do-you-track-all-sales-related-activities-in-crm)

What stuff do you need to store?

For most projects, you need to quickly store and locate important details and documents such as:

* Server details (Dev, Test, Production)
* Change-log documents
* Upcoming features (most often in Word or OneNote)
* General documents e.g. Requirements/Specifications (Note: it is possible to share documents from Microsoft Teams externally, but not from Teams directly... just open it in Office Online or a specific Office app first)



<dl class="badImage"><dt> 
      <img alt="Keep Files Bad Example" src="Dont-keep-files.jpg"> 
   </dt><dd>Figure: Bad example – It might be easy to use File Shares, your Local C: or emails – but don’t. They don’t work in a team environment as they aren’t easy for others to access</dd></dl><dl class="badImage"><dt> 
      <img alt="Keep Files Bad Example" src="keep-files-TFS.jpg"> 
   </dt><dd>Figure: Bad example – SharePoint integrated into Azure DevOps (was VSTS/TFS) is not supported via Visual Studio anymore</dd></dl><dl class="badImage"><dt> 
      <img alt="Keep Files Bad Example" src="keep-files-SP.jpg"> 
   </dt><dd>Figure: Bad example – even though this is using SharePoint - this is using a Team Site with a Document Library - it is better to use Microsoft Teams which uses SharePoint under the covers</dd></dl><dl class="goodImage"><dt> 
      <img alt="Keep Files Good Example" src="keep-files-sp-teams.jpg"> 
   </dt><dd>Good example: Use Microsoft Teams and it will automatically create a Site for the Team (and that includes a document library which you can connect to with OneDrive)</dd></dl>
### What does not get stored in Microsoft Teams? 


1.	For developers,


> A: code obviously belongs in GitHub, Azure DevOps, etc.
> 
> B: Also the [7 important documents](/do-you-review-the-documentation) should be stored in Azure DevOps (was TFS/VSTS)... or instead        [use Markdown with the Wiki](/do-you-make-getting-started-on-a-project-easy-for-new-developers)


2.	For designers with large files, OneDrive is a better choice. See: [Do you know the best Source Control for Designers?](/do-you-know-the-best-source-control-for-designers)

### What about usernames and passwords?


Documents with user names and passwords should not be stored in Microsoft Teams. Security is very important for everyone and every company. Use Azure KeyVault or [KeePass](http://keepass.info/) to store usernames and passwords. KeePass keeps all passwords in one database locked by a master key, which should be accessible only by the few people you trust.



### Related rule


* Do you integrate Dynamics 365 and Microsoft Teams?
