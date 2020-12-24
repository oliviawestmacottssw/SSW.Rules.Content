---
type: rule
archivedreason: depreciated
title: How to use SSW style in RadHtmlControl?
guid: d7f9ffd2-878b-484f-8e3e-4574fb666c30
uri: how-to-use-ssw-style-in-radhtmlcontrol
created: 2010-02-02T17:36:43.0000000Z
authors:
- id: 1
  title: Adam Cogan
related: []
redirects: []

---

Do you know how to apply style to image, figure..etc?

Let's take the "AvoidReplyToAllWhenBcc" page as example.

<!--endintro-->
 First, the reason to cause the style issue is the style doesn’t apply to right place. Below is the html code after you adjust the figure manually (sorry, still not right ). Please look at the highlight part, 

* the “ms-rteCustom-ImageArea” style doesn’t apply to 
![]() tag, but wrapped by  with “ms-rteCustom-ImageArea” style;


* there is no style apply to figure;


<font class="ms-rteCustom-CodeArea"><span class="ms-rteCustom-YellowBorderBox">We have a program called <a href="<a shape=" rect"="" href="/WebSites/RulesToBetterWebsitesLayout">http://rules.ssw.com.au/WebSites/RulesToBetterWebsitesLayout</a>"><br>
        SSW LookOut! for Outlook to check for this rule.<br>
        <br><br>
        <br><br>
       <font class="ms-rteCustom-Highlight"><span class="ms-rteCustom-ImageArea"><br>
</span></font>            <img style="border-bottom: 0px solid; border-left: 0px solid; border-top: 0px solid;<br>
                border-right: 0px solid;" border="0" alt="Lookout Reply All BCC Warning" src="<a shape=" rect"="" href="/WebSites/RulesToBetterWebsitesLayout">http://rules.ssw.com.au/WebSites/RulesToBetterWebsitesLayout" /><br>
            <br><br>
       <font class="ms-rteCustom-Highlight"></font></span></font> **


<br>            Figure: SSW LookOut! for Outlook warns you if you accidentally 'Reply All' when
<br>            you have been BCC'ed** 
 1.  Not sure how user inputs the  content into this page. Anyway, here is the right way to add content via Telerik Editor. Please read below example of how I redo this part in Telerik Editor without changing the code manually

![Copy content in the notepad 2. Delete the current content from Telerik for a new start;](SaveContentInNotePad.jpg)

 3. Copy the first sentence from notepad and paste into Telerik Editor in the page; (please avoid copying straightly from web page and pasting them here, it will copy the all tags as well. it might affect the styles which can’t apply correctly )

![Start copying content over 4. Insert the image](CopyFromNotePad.jpg)

![Add a link to text 5. Add an image](InsertImage.jpg)

![Inser an image 6. Press “enter” key to start a new row, then copy the figure from notepad to the Telerik editor area](ApplyStyleInsertImage.jpg)

![Add figure 7. Apply image style to the image by click on the image, then choose a style from “Apply CSS Class” dropdown list](ApplyStyleAddFigure.jpg)

![Apply style to the image](ApplyStyleImageArea.jpg)
** 
 8. Apply style to the figure

![Apply style to the figure 9.Apply the yellow box](ApplyStyleImageArea.jpg)

![Apply yellow border box to the content 10. Check in the changes, then you will have - "dada.."](ApplyStyleFigure.jpg)

![Right style in use](ApplyStyleResult.jpg)
