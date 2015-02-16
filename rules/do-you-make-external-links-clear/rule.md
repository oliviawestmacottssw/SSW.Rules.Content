---
type: rule
title: Do you make external links clear?
uri: do-you-make-external-links-clear
created: 2015-02-16T02:21:22.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 16
  title: Tiago Araujo

---

 
When I create links I follow a few basic rules:
 
1. If a link is to an external site, a visual indication should be provided to the user like this: <br>      [This is a link to another site](http&#58;//www.ssw.com.au/ssw/Redirect/Microsoft/microsoft.htm). <br>      
Search Engines ([http://www.google.com](http&#58;//www.ssw.com.au/ssw/Redirect/Web/Google.htm) is by far the best but try other search engines as well)
Figure: Bad example - Without visual indication
Search Engines ([http://www.google.com](http&#58;//www.ssw.com.au/ssw/Redirect/Web/Google.htm) is by far the best but try other search engines as well)
Figure: Good example - With visual indication
2. All external links should NOT open in a New Window - this behaviour should be up to the user's discretion and not pre-determined by your site. New windows opening without the user's permission is considered spam behaviour.
3. External links should always go through a Redirect file to allow monitoring of click-throughs. We store all redirects in a redirect folder - /ssw/Redirect/[SubCategoryAsRequired] to <br>      [avoid reducing our Google Ranking](http&#58;//www.ssw.com.au/ssw/Standards/Rules/RulesToBetterGoogleRankings.aspx#Robotstxtfile). <br>          **Developer Note:** Do not use META refresh - instead, use server-side code (such as an ASP Response.Redirect), as this will send the proper "Object moved" message to the client and the redirect will be picked up by           [SSW Link Auditor](http&#58;//www.ssw.com.au/ssw/Standards/DeveloperGeneral/WebdevelopmentTools.aspx#BrokenLinks). There is also the possibility that the user has disabled META refreshes in the browser security options, as the redirect is performed on the client, not the server.

Microsoft Knowledge Base -              [http://support.microsoft.com/support](http&#58;//support.microsoft.com/support) (Great for issues/bugs in your programs)
Figure: Bad example - Go through a direct link
Microsoft Knowledge Base -              [http://support.microsoft.com/support](http&#58;//www.ssw.com.au/ssw/Redirect/Microsoft/MicrosoftSupport.htm) (Great for issues/bugs in your programs)
Figure: Good example - Go through a redirect file &lt;% Response.Redirect("http://www.link.com") %&gt; Figure: Sample Code for a Redirect File
4. External link images should be inserted by CSS and not embedded in the page source. <br>      ![](http&#58;//www.ssw.com.au/SSW/Standards/Rules/images/BadLink.gif)Figure: Bad example - Why is this in my source code?![](http&#58;//www.ssw.com.au/SSW/Standards/Rules/images/GoodLink.gif)Figure: Good example - Icon is added by CSS via a simple declaration.


We have a program called     [SSW Code Auditor](http&#58;//www.ssw.com.au/ssw/CodeAuditor/) to check for this rule.

