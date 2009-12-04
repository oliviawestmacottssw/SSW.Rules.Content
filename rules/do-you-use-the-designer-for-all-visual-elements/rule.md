---
type: rule
title: Do you use the designer for all visual elements?
uri: do-you-use-the-designer-for-all-visual-elements
created: 2009-04-28T02:20:39.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 17
  title: Ryan Tee

---

 This field should not be null (Remove me when you edit this field). 
Things that do not belong in the designer:

- Connections
- Commands
- DataAdapters


However, and **DataAdapter** objects should not be dragged onto forms, as they belong in the business tier. Strongly typed **DataSet** objects should be in the designer as they are simply passed to the business layer. Avoid writing code for properties that can be set in the designer.
![](/Standards/SoftwareDevelopment/RulesToBetterDotNETProjects/PublishingImages/BadDesigner.gif) Bad example - Connection and Command objects in the Designer ![](/Standards/SoftwareDevelopment/RulesToBetterDotNETProjects/PublishingImages/GoodDesigner.gif) Good example - Only visual elements in the designer
