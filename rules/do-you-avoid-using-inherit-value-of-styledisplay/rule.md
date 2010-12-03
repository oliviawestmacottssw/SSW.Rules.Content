---
type: rule
title: Do you avoid using "inherit" value of style.display?
uri: do-you-avoid-using-inherit-value-of-styledisplay
created: 2010-12-02T10:35:22.0000000Z
authors: []

---

 The property “inherit” of JavaScript is not recognized by IE7 and IE7 compatibility mode. So if you use this property, it always causes script error in IE7 and IE compatibility. <br> 

```
divLoading.style.display = "inherit";
```

Bad code - inherit property 

```
divLoading.style.display = "block";
```

Good code - block property 
