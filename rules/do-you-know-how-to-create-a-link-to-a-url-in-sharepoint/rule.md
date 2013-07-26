---
type: rule
title: Do you know how to create a link to a URL in SharePoint?
uri: do-you-know-how-to-create-a-link-to-a-url-in-sharepoint
created: 2013-07-26T00:38:30.0000000Z
authors:
- id: 9
  title: William Yin
- id: 1
  title: Adam Cogan

---

 ​You may need a link in a SharePoint document to help you navigate to a different URL (like shortcut in Windows), there are different ways to implement this.


A. ​Create a shortcut in windows, then upload the shortcut file (.url) to the document library.B. Use "Link to a document" content type in SharePoint.


 
Step details:​

**A. Create a shortcut in windows, then upload the shortcut file (.url) to the document library.​**

To do this, you need to remove .url file type from your blocked file types in your web application, this will bring some security risk, which is not recommended, and I won't show the step details here.

**B. Use "Link to a document" content type in SharePoint.**

1) Enable "Content Type management"​ in your document library.
![EnableContentTypeDocument.png](/ITAndNetworking/SharePoint/SiteAssets/Pages/LinkToADocument/EnableContentTypeDocument.png)Figure: Enable Conent Type management in library setting
2) Add "Link to a Document" content type into the library.
![AddExistContentType.png](/ITAndNetworking/SharePoint/SiteAssets/Pages/LinkToADocument/AddExistContentType.png)Figure: Add from existing site content type![SelectLinkToADocumentType.png](/ITAndNetworking/SharePoint/SiteAssets/Pages/LinkToADocument/SelectLinkToADocumentType.png)Figure: Select "Link to a Docuemnt" content type
3) Create a "Link to a docuemnt" instance
![CreateLinkToADocumentInstance.png](/ITAndNetworking/SharePoint/SiteAssets/Pages/LinkToADocument/CreateLinkToADocumentInstance.png)Figure: select "File | New Document (dropdown) | Link to a document"![InputLinkUrlAndName.png](/ITAndNetworking/SharePoint/SiteAssets/Pages/LinkToADocument/InputLinkUrlAndName.png)Figure: Input "Name" and "URL"
​4) Done

You should be able to see the link type document in your library:
![LinksTypeDocumentsWithShortcutIcon.png](/ITAndNetworking/SharePoint/SiteAssets/Pages/LinkToADocument/LinksTypeDocumentsWithShortcutIcon.png)Figure: Link type documents with the lovely shortcut icon


