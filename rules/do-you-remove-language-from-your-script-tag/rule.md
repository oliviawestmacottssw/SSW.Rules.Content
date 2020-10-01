---
type: rule
title: Do you remove "Language" from your script tag?
uri: do-you-remove-language-from-your-script-tag
created: 2012-07-24T18:10:04.0000000Z
authors:
- id: 16
  title: Tiago Araujo

---

A few years ago, it was common to have the "language" attribute within the script tags. This attribute was used to specify the scripting language of the contents of this element.
 
Since these identifiers are not standard, this attribute has been deprecated in favor of "type".


&lt;script href="script.js" language="javascript"&gt;&lt;/script&gt;

Figure: Language attribute has been deprecated

&lt;script href="script.js" type="text/javascript"&gt;&lt;/script&gt;

Figure: The scripting language is specified as a content type
Read more on [W3C website](http&#58;//www.w3.org/TR/html4/interact/scripts.html#h-18.2.2).
