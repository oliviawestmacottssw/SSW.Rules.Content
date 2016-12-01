---
type: rule
title: Do you know the best Source Control for designers?
uri: do-you-know-the-best-source-control-for-designers
created: 2014-03-03T04:11:03.0000000Z
authors:
- id: 20
  title: Rebecca Liu
- id: 1
  title: Adam Cogan

---


​When it comes to the easiest and quickest<br>way to share files between designers, it should all be done in Dropbox.
 ![](/PublishingImages/Designer-Source-Control-TFS.png) Figure: Bad example – TFS takes too long to set up and too slow to use
 ![](/PublishingImages/Designer-Source-Control-SkyDrive.png) Figure: Bad Example – What seemed like a great idea at the time, SharePoint and SkyDrive proved to be plagued with slow response times, upload errors and unresponsiveness
 ![](/PublishingImages/Designer-Source-Control-DropBox.png) Figure: Good Example – Dropbox… the way file sharing is meant to be

### So why do we prefer Dropbox over OneDrive?


1. **OneDrive (was SkyDrive) requires me to check out the file in SharePoint before I make changes. **    I have to open a web browser, log in to the intranet, check out the file, and then open the file on my computer before I can make edits to it. This is a shocking amount of busy work for something that is already on my computer. I am unable to work directly from the file on my computer and have it sync automatically. I have to check out a file that is ON my computer. Why can I not check out the file from my computer? Why does it not check out the file when I edit it?
    Dropbox lets me work right away on the file on my computer
 ![](/PublishingImages/Designer-Source-Control-SkyDriveCheckout.png) Figure: OneDrive (was SkyDrive) has no option to "check out" here. I have to go to the browser and check out a file which is on my computer. Better yet, Dropbox doesn't even ask me to check out, it just does it
2. **For me to check out the file and to upload the file to "SharePoint" I have to be on VPN. **    Our VPN speed is horrible for people outside of Sydney and it takes me the majority of the day to upload 1 Photoshop file. This is unacceptable, because the files designers work with are huge. I.E. those posters of Uly, Mehmet and William are  54MB… EACH.
    I can use Dropbox and have it sync to Tiago, David, without needing to be on VPN. The files are sync'd as I work so they are never out of date, or "waiting to be uploaded"
3. **When OneDrive (was SkyDrive) has an error, it just sits there and pauses my other files until the error is resolved. **    Even if the problem is something like "this file is too big for upload." Somehow one large file prevents my other normal files from being uploaded.
    I have used Dropbox for 3 years and it has never given me an error.
 ![](/PublishingImages/Designer-Source-Control-SkyDriveUploadPaused.png) Figure: OneDrive (was SkyDrive) has my last two files just sitting as "upload paused" – these files are perfectly ok to be uploaded but it refuses to do so, even when I ask it to
4. ** OneDrive (was SkyDrive) has strange errors that cannot be resolved. **    For example, in the screenshot below, I have been getting "Upload pending" when I have repeatedly tried to upload the file. I have no idea what OneDrive is doing. The file is checked out in SharePoint, it's a little big but typical of designer files. And yet, OneDrive sits there, doing nothing and throwing me popup messages about the status being updated.
    Dropbox just works.
![](/PublishingImages/Designer-Source-Control-SkyDriveLoop.png) Figure: In OneDrive (was SkyDrive), my files are stuck in a "Upload pending" loop. I do not know why, as the files have been checked out and are not particularly large
5. ** OneDrive (was SkyDrive) has problems uploading files. **    

    - In the first box, it decided to upload my file as a new file instead of saving the old one as a version
    - In the second box, it **overrode** my file with something that has no file size (probably a broken file.)

    
    Thank god that second file is saved in my Dropbox. Dropbox has never broken my files and it knows how to save files with version tracking.
 ![](/PublishingImages/Designer-Source-Control-SkyDriveError.png) Figure: OneDrive (was SkyDrive) has both failed to save a file as a new version and uploaded a truncated file


Of course, Dropbox is not perfect. There is the issue of file size limit, especially as the Share Folder takes up a portion of the individual user's account (this is resolved by upgrading to a [Dropbox Business Account](https&#58;//www.dropbox.com/help/59/en)). A free account starts off with only 2GB and this is likely not enough especially as your team's shared folder continues to get bigger.

For developers, see: [Do you know where to keep your files - TFS, SharePoint?](/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=2860239f-9812-414a-ad42-6174c928cbb0)

