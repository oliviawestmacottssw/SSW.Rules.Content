---
type: rule
title: Do you know where to keep your files?
uri: do-you-know-where-to-keep-your-files
created: 2011-08-29T19:18:47.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 16
  title: Tiago Araujo
- id: 66
  title: Liam Elliott

---

 ​Each client project should have a nice place to keep files. In the old days, things were simple but limited, we simply used Windows Explorer and file shares. Today there are so many places that teams can store documents e.g. Dropbox, OneDrive, SharePoint, TFS, and even Microsoft Teams.
 
### Which is the best corporate solution?


The solution that allows the best collaboration with Developers, Project Managers, and other stakeholders is SharePoint and Microsoft Teams. It is super easy to create, upload and share documents with others.

### What stuff do you need to store?​


For most projects you need to quickly store and locate important details and documents such as:

- Server details (Dev, Test, Production)
- Change-log documents
- Upcoming features (most often in Word or OneNote)
- General documents e.g. Requirements/Specifications (Note: it is possible to share documents from Microsoft Teams externally, but not from Teams directly... just open it in ​Office Online or a specific Office app first)​



![Keep Files Bad Example](/PublishingImages/Dont-keep-files.jpg)Figure: Bad example – It might be easy to use File Shares, your Local C: or emails – but don’t. They don’t work in a team environment as they aren’t easy for others to access![Keep Files Bad Example](/PublishingImages/keep-files-TFS.jpg)Figure: Bad example – SharePoint integrated into TFS is not supported via Visual Studio anymore![Keep Files Bad Example](/PublishingImages/keep-files-SP.jpg)Figure: Bad example – even though this is using SharePoint - this is using a Team Site with a Document Library - it is better to use Microsoft Teams which uses SharePoint under the covers![Keep Files Good Example](/PublishingImages/keep-files-sp-teams.jpg)Good example: Use Microsoft Teams and it will automatically create a Site for the Team (and that includes a document library which you can connect to with OneDrive)
### What does not get stored in Microsoft Teams? 


1. For developers, the [6 important documents](/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=951ffbf9-4066-42f3-a9b7-e0d8603e728b) should be stored in Azure DevOps (was TFS/VSTS).​​.. or instead [use Markdown with the Wiki](/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=846474eb-27a1-4645-90ee-10a349fef714)
2. For designers with large files, OneDrive is a better choice. See: [Do you know the best Source Control for Designers?](/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=2df3378d-f923-4f3f-8c86-ec1074f7f98b)

### What about usernames and pas​swords?


Documents with user names and passwords should not be stored in Microsoft Teams. Security is very important for everyone and every company. Use Azure KeyVault or [KeePass](http&#58;//keepass.info/) to store usernames and passwords. KeePass keeps all passwords in one database locked by a master key, which should be accessible only by the few people you trust.

