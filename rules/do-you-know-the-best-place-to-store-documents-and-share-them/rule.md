---
type: rule
title: Do you know the best place to store documents and share them?
uri: do-you-know-the-best-place-to-store-documents-and-share-them
created: 2018-07-30T01:05:40.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 78
  title: Matt Wicks
- id: 69
  title: Jean Thirion

---

There is a myriad of options to choose from when storing and sharing documents, some examples include:

- SharePoint
- OneDrive or Dropbox or Google Drive
- Microsoft Teams | Team Site

The best choice is Microsoft Teams because it brings together the best of SharePoint, cloud file storage, real time collaboration and more into a single location.


 
[[badExample]]
| ![You shouldn't look for files on network shares](teams - network share.png)
[[goodExample]]
| ![You can use the files tab in Teams](teams - file tab.png)(without leaving the app)
The great thing about having conversations next to the file is that it is always in context. Also, future users can view the conversation when they open the file in teams.

[[goodExample]]
| ![You can have a conversation about a file](teams - document conversation.png)
Behind the scenes, storage is provided by a SharePoint site; so that is there if you want to use it. As an added bonus thanks to this; you can take the files offline by syncing with OneDrive for Business and by default each channel gets its own folder.

[[goodExample]]
| ![You can open the files in SharePoint](teams - open sharepoint.png)
[[goodExample]]
| ![You can sync the files in SharePoint with your current machine through OneDrive. A toast notification should popup indicating that files will be synced.](teams - sync onedrive.png)
**Note:** You can add other cloud storage providers for file storage e.g. Google Drive, Dropbox, etc     
This is not recommended - as they aren't first-class citizens i.e. if you want to share files from them, you need to go to the provider's sharing settings outside of Teams


**Warning:** By using Teams instead of SharePoint, you are losing a number of key features:
- No full fidelity support for Metadata in Document Libraries e.g. can’t add extra columns into the “Files” tab
- No support for private channels e.g. you will need a team per subset of users with different permissions
- No direct access to version history from Teams UI (still exists on SharePoint UI)
- No access to the cross-office365 Search feature e.g. SharePoint search is better (see video: <br>         https://youtu.be/TiWzzdASVWE)
- No access to external content in the search feature e.g. can’t search rules.ssw.com.au
- No access to SharePoint designer workflows (although the new way to do it is Microsoft Flow)
