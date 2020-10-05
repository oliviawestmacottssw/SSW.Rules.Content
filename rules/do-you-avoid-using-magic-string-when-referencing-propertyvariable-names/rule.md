---
type: rule
title: Do you avoid using magic string when referencing property/variable names
uri: do-you-avoid-using-magic-string-when-referencing-propertyvariable-names
created: 2020-01-29T05:00:13.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 66
  title: Liam Elliott

---

​Hard coded strings when referencing property and variable names can be problematic as your codebase evolves, and can make your code brittle.
 
​​(if customer.Address.ZipCode == null) throw new ArgumentNullException("ZipCode");
Figure: ​​​Bad Example - Hardcoding a reference to a property

​​(if customer.Address.ZipCode == null) throw new ArgumentNullException(nameof(customer.Address.ZipCode));
​​Figure: Good Example - Using nameof() operator to avoid hardcoded strings
