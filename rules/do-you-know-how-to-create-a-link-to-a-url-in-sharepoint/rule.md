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

TODO TIAGO: ADD IMAGE OF WINDOWS EXPLORER (4 files in it) AND ANOTHER WITH SHAREPOINT DOCUMENTS LIBRARY




You may need a link in a SharePoint document to help you navigate to a different URL (like shortcut in Windows), there are different ways to implement this.


A.  Create a shortcut in windows, then upload the shortcut file (.url) to the document library.B. Use "Link to a document" content type in SharePoint.



 
Details on how you to create a link to a document in a SharePoint library.

**A. Create a shortcut in windows, then upload the shortcut file (.url) to the document library. **

To do this, you need to remove .url file type from your blocked file types in your web application. This will bring some security risk, which is not recommended, and I won't show the step details here.

**B. Use "Link to a document" content type in SharePoint.**

1) Enable "Content Type management" in your document library.

![Enable Content Type management in library setting](EnableContentTypeDocument.png)
2) Add "Link to a Document" content type into the library.

![Add from existing site content type](AddExistContentType.png)
![Select "Link to a Document" content type](SelectLinkToADocumentType.png)
3) Create a "Link to a document" instance

![select "File | New Document](CreateLinkToADocumentInstance.png)(dropdown) | Link to a document"
![Input "Name" and "URL"](InputLinkUrlAndName.png)
4) Done

You should be able to see the link type document in your library:

![Link type documents with the lovely shortcut icon](LinksTypeDocumentsWithShortcutIcon.png)
