---
type: rule
title: Do you use icons not to surprise users (aka use the correct image for files)?
uri: do-you-use-icons-not-to-surprise-users-aka-use-the-correct-image-for-files
created: 2015-02-16T02:46:02.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 16
  title: Tiago Araujo

---

 
When a user clicks on a hyperlink they expect to open an HTML​ file. If you click on a hyperlink (but it is actually a .doc file) you wait and wait while it takes forever to instantiate an instance of Microsoft Word in the background.
 
Don't surprise users! Use the following icons:


| File Type | Example |
| --- | --- |
| PDF | ![Icon PDF](../../assets/IconPdf.png) This is a PDF file<br> |
| JPG | ![Icon JPG](../../assets/IconJpg.gif) This is an Image file |
| DOC or DOT | ![Icon DOC](../../assets/IconDoc.png) This is a Word Document file |
| XLS | ![Icon XLS](../../assets/IconXls.gif) This is an Excel Spreadsheet file |
| PPT | ![Icon PPT](../../assets/IconPPT.png) This is a PowerPoint file |
| TXT | ![Icon TXT](../../assets/IconTxt.gif) This is a Text file |
| AVI, MOV, MPG etc. | ![Icon MOV](../../assets/IconMov.gif) This is a Video file |
| WAV, WMA, MP3 etc. | ![Icon MP3](../../assets/IconMus.gif) This is a Music file |
| SNP | ![Icon SNP](../../assets/IconSnp.gif) This is an Access Database snapshot file (discontinued and not recommended) |
| EPS | ![Icon EPS](../../assets/IconEps.gif) This is an EPS file |
| ICS or VCS | ![Icon VCS](../../assets/IconVCS.gif) This is a calendar file |
| EXE or ZIP | ![Download](../../assets/Download.gif)This is an executable or zip file |
| Mailto: | ![Icon MailTo](../../assets/IconMailTo.gif) This will send an email |
| XML / RSS | ![Icon XML](../../assets/IconXML.gif) This will subscribe to RSS |
| ODF | ![Icon ODF](../../assets/IconOFT.gif) This is an Outlook Item Template |
| Page | ![](../../assets/ms_lock.gif) This is a link to password protected page |
| YouTube | ​![](youtube-icon_png.jpg)This is a link to a YouTube Video |

 ![Image good link](../../assets/GoogleIcons.gif) Figure: FYI there are the same images used by Google at [GoogleDesktopSideBar.htm](http://desktop.google.com/features.html)
  ![Image bad link](../../assets/IconImageBad.gif) Figure: Bad Example - The user would expect all these hyperlinks to work the same way
  ![Image good link](../../assets/IconImageGood.gif) Figure: Good Example - The pdf icon (before a hyperlink) indicates it is not a web page

### How to add an icon before a link with CSS

Add the icon image to your server. Then use $= to make the match the extension of the >a< tag on your CSS. The padding is to give it some space before the text (where the icon will be).

a[href$='.pdf'] 
{ 
background: transparent url(/images/icon\_pdf.gif) center left no-repeat; 
padding-left: 20 px; 
}



We have the programs [SSW CodeAuditor](http://www.codeauditor.com/) and [SSW LinkAuditor](https://linkauditor.com.au/) to check for this rule.


