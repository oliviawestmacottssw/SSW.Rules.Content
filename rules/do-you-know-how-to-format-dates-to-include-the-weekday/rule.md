---
type: rule
title: Do you know how to format dates to include the weekday?
uri: do-you-know-how-to-format-dates-to-include-the-weekday
created: 2009-06-26T10:07:46.0000000Z
authors:
- id: 9
  title: William Yin

---

 This field should not be null (Remove me when you edit this field).   To achieve this , you can :  
Step1:  List Settings - columns -Create column - Calculated (calculation based on other columns),then you can see the columns of this list in the "Insert Column", add the column you want to change format,  and custom the code in "Formula" like below:

![](/Standards/CodeAndApplicationDesign/RulesToBetterSharePoint/PublishingImages/CalculatedColumnWithFormulaCode.gif)
Figure: Calculated column with Formula code.

Step2: Change the views of the list to use the new Calculated column(WeekDate) instead of the original date column(Date):

![](/Standards/CodeAndApplicationDesign/RulesToBetterSharePoint/PublishingImages/ReplaceOldDate.gif)
Figure: Replace the old Date column(Date) with new Calculated column(WeekDate).

