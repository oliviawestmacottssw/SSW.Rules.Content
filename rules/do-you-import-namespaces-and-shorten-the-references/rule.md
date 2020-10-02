---
type: rule
title: Do you import namespaces and shorten the references?
uri: do-you-import-namespaces-and-shorten-the-references
created: 2018-04-25T22:28:24.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

You should import namespaces and shorten the references.
 
System.Text.StringBuilder myStringBuilder = new System.Text.StringBuilder();
Figure: Bad code - Long reference to object name

using System.Text;
...
...
StringBuilder myStringBuilder = new StringBuilder();
Figure: Good code - Import the namespace and remove the repeated System.Text reference



If you have ReSharper installed, you can let ReSharper take care of this for you:

![ Right click and select "Reformat Code..."](ReSharperReformatCode.gif)


![ Make sure "Shorten references" is checked and click "Reformat"](ReSharperShortenReferences.gif)
