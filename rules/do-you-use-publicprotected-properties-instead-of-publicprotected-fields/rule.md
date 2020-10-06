---
type: rule
title: Do you use Public/Protected Properties instead of Public/Protected Fields?
uri: do-you-use-publicprotected-properties-instead-of-publicprotected-fields
created: 2018-04-25T21:45:02.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

Public/Protected properties have a number of advantages over public/protected fields:

- **Data validation**
Data validation can be performed in the get/set accessors of a public property. This is especially important when working with the Visual Studio .NET Designer.
- **Increased flexibility**
Properties conceal the data storage mechanism from the user, resulting in less broken code when the class is upgraded. Properties are a recommended object-oriented practice for this reason.
- **Compatibility with data binding**
You can only bind to a public property, not a field.
- **Minimal performance overhead**
The performance overhead for public properties is trivial. In some situations, public fields can actually have inferior performance to public properties.

 
public int Count;
Figure: Bad code. Variable declared as a Field

public int Count
{
 get
 {
 return \_count;
 }
 set
 {
 \_count = value; 
 }
}
Figure: Good code. Variable declared as a Property

We agree that the syntax is tedious and think [Microsoft should improve this.](https&#58;//www.ssw.com.au/ssw/Standards/BetterSoftwareSuggestions/VisualStudio.aspx#PropertyShortcut)
