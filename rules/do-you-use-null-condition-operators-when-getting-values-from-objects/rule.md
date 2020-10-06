---
type: rule
title: Do you use null condition operators when getting values from objects
uri: do-you-use-null-condition-operators-when-getting-values-from-objects
created: 2020-01-29T05:20:27.0000000Z
authors:
- id: 66
  title: Liam Elliott
- id: 78
  title: Matt Wicks

---

Null-conditional operators - makes checking for null as easy as inserting a single question mark. The Null-conditional operators feature boils down all of the previously laborious clunky code into a single question mark.
 
int length = customer != null && customer.name != null ? customer.name.length : 0;
Figure: Bad Example - Verbose and complex code checking for nulls

int length = customers?.name?.length ?? 0;
Figure: Good Example - Robust and easier to read code
