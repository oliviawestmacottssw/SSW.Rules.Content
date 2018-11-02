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

 Creating, uploading, and sharing documents with other people should be done using SharePoint and Microsoft Teams.
 
In the old days, we used File Shares. Today there are so many places that teams can store documents eg. Dropbox, OneDrive, SharePoint, TFS, and even Microsoft Teams.

The solution should allow collaboration with Developers, Project Managers, and other stakeholders.

You want to be able to quickly store and locate important details such as:

- Server details (Dev, Test, Production)
- Changelogs
- Upcoming features


### Documents


- Requirements/Specifications


### Additional Information

- Server settings

 ![Keep Files Bad Example](/PublishingImages/Dont-keep-files.jpg) Figure: Bad example – File Share or your Local C: or emails - they aren’t easy for others to access ![Keep Files Bad Example](/PublishingImages/keep-files-TFS.jpg) Figure: Bad example – Sharepoint integrated into TFS is not supported via Visual Studio anymore ![Keep Files Bad Example](/PublishingImages/keep-files-SP.jpg) Figure: Bad example – even though this is using SharePoint - this is using a Team Site with a Document Library - it is better to use Microsoft Teams which uses SharePoint under the covers  ![Keep Files Good Example](/PublishingImages/keep-files-sp-teams.jpg) Good example: Use Teams and it will automatically create a Site for the Team (and that includes a document library and Team OneDrive)
**Note: **[4 important documents](/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=951ffbf9-4066-42f3-a9b7-e0d8603e728b)should be stored in TFS.​​

For designers, see: [Do you know the best Source Control for Designers?](/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=2df3378d-f923-4f3f-8c86-ec1074f7f98b)


### What about usernames and passwords?

Security is very important for any company. You should use [KeePass](http&#58;//keepass.info/) to store usernames and passwords. KeePass keeps all passwords in one database locked by a master key, which should be accessible only by the few people you trust.


