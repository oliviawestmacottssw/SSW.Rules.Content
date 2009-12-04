---
type: rule
title: Do you use jQuery for making a site come alive?
uri: do-you-use-jquery-for-making-a-site-come-alive
created: 2009-08-25T00:13:02.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

 This field should not be null (Remove me when you edit this field). ![Bad example – there is no response when mouse is over the image](/Standards/WebSites/RulesToBetterWebsiteDevelopmentASPDotNet/PublishingImages/OldFashionSite.jpg) Figure: Bad example – there is no response when mouse is over the image ![Good example – apply the different style when mouse is over](/Standards/WebSites/RulesToBetterWebsiteDevelopmentASPDotNet/PublishingImages/NewFashionSite.jpg) Figure: Good example – apply the different style when mouse is over 

```
$("p").hover(function () {
            $(this).css({ "background-color":"yellow", "font-weight":"bolder" }); },
            function () { 
                var cssObj = { "background-color": "#ddd", 
                "font-weight": "", 
                color: "rgb(0,40,244)"
            }
            $(this).css(cssObj);
        });
```

Figure: Mouse hover sample 
