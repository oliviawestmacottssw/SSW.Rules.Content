---
type: rule
title: Do you avoid using "inherit" value of style.display?
uri: do-you-avoid-using-inherit-value-of-styledisplay
created: 2010-12-02T10:35:22.0000000Z
authors: []

---

The property value “inherit” of style.display is not recognized by IE7 and IE7 compatibility mode. So if you use this value in Javascript, it will cause script error in IE7 and IE7 compatibility like: 
<br>            "Message: Could not get the display property. Invalid argument." 
<br>So to make your Javascript and CSS style more compatible and avoid using "inherit" value of style.display:<br> 

```
divLoading.style.display = "inherit";
```

Bad code - inherit property 

```
divLoading.style.display = "block";
```

Good code - block property
