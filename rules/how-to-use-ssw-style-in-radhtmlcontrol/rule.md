---
type: rule
title: How to use SSW style in RadHtmlControl?
uri: how-to-use-ssw-style-in-radhtmlcontrol
created: 2010-02-02T17:36:43.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

Do you know how to apply style to image, figure..etc?

Let's take the "AvoidReplyToAllWhenBcc" page as example.
  First, the reason to cause the style issue is the style doesn’t apply to right place. Below is the html code after you adjust the figure manually (sorry, still not right ). Please look at the highlight part, 

- the “ms-rteCustom-ImageArea” style doesn’t apply to 
![]() tag, but wrapped by  with “ms-rteCustom-ImageArea” style;


- there is no style apply to figure;


We have a program called [http://rules.ssw.com.au/WebSites/RulesToBetterWebsitesLayout](/WebSites/RulesToBetterWebsitesLayout)">
<br>        SSW LookOut! for Outlook to check for this rule.






![](<a shape=)http://rules.ssw.com.au/WebSites/RulesToBetterWebsitesLayout" />


**


<br>            Figure: SSW LookOut! for Outlook warns you if you accidentally 'Reply All' when
<br>            you have been BCC'ed **
 1.  Not sure how user inputs the  content into this page. Anyway, here is the right way to add content via Telerik Editor. Please read below example of how I redo this part in Telerik Editor without changing the code manually

![Copy content in the notepad2. Delete the current content from Telerik for a new start;](SaveContentInNotePad.jpg)


 3. Copy the first sentence from notepad and paste into Telerik Editor in the page; (please avoid copying straightly from web page and pasting them here, it will copy the all tags as well. it might affect the styles which can’t apply correctly )

![ Start copying content over4. Insert the image](CopyFromNotePad.jpg)


![ Add a link to text5. Add an image](InsertImage.jpg)


![ Inser an image6. Press “enter” key to start a new row, then copy the figure from notepad to the Telerik editor area](ApplyStyleInsertImage.jpg)


![ Add figure7. Apply image style to the image by click on the image, then choose a style from “Apply CSS Class” dropdown list](ApplyStyleAddFigure.jpg)


![ Apply style to the image](ApplyStyleImageArea.jpg)


 8. Apply style to the figure

![ Apply style to the figure9.Apply the yellow box](ApplyStyleImageArea.jpg)


![ Apply yellow border box to the content10. Check in the changes, then you will have - "dada.."](ApplyStyleFigure.jpg)


![ Right style in use](ApplyStyleResult.jpg)
