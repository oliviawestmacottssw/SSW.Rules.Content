---
type: rule
title: Do you use jQuery for making a site come alive?
uri: do-you-use-jquery-for-making-a-site-come-alive
created: 2009-08-25T00:13:02.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

To please customers every business knows they need to keep their services and offerings fresh and up-to-date. The same is true for websites. In order to attract new traffic, we should make the website vivid. <br> 
[[badExample]]
| ![ Bad example – there is no response when mouse is over the image ](OldFashionSite.jpg) 

[[goodExample]]
| ![ Good example – apply the different style when mouse is over ](NewFashionSite.jpg) 


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
