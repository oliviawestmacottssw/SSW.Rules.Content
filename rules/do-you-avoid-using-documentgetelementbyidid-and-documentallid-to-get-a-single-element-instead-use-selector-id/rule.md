---
type: rule
title: Do you avoid using document.getElementById(id) and document.all(id) to get a single element, instead use selector $(#id)?
uri: do-you-avoid-using-documentgetelementbyidid-and-documentallid-to-get-a-single-element-instead-use-selector-id
created: 2016-11-17T15:17:08.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

 
$(#id) is a selector of jQuery. It gets the single element with the given id.

[jQuery](http&#58;//jquery.com/) ​is a fast and concise JavaScript Library that simplifies how you traverse HTML documents, handle events, perform animations, and add Ajax interactions to your web pages. jQuery is designed to change the way that you write JavaScript.​
 
​With jQuery, you can write less code but do more work.

&lt;h1 id="Head1"&gt;Hello&lt;/h1&gt; 
&lt;script type="text/javascript" language="javascript"&gt;
    document.all("Head1").style.color="red"; 
&lt;/script&gt;
Figure - Bad Code​​​
&lt;h1 id="Head1"&gt;Hello&lt;/h1&gt; 
&lt;script type="text/javascript" language="javascript"&gt;​​
    document.getElementById("Head1").style.color="red"; 
&lt;/script&gt;
Figure: Bad Code​
&lt;h1 id="Head1"&gt;Hello&lt;/h1&gt; 
&lt;script type="text/javascript" language="javascript"&gt;
    $("#Head1").css("color","red"); 
​&lt;/script&gt;
Figure: Good Code - Using $("#Head1")​​​

