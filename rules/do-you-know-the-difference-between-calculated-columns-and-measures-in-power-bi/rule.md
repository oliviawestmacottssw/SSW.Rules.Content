---
type: rule
title: Do you know the difference between Calculated Columns and Measures in Power BI?
uri: do-you-know-the-difference-between-calculated-columns-and-measures-in-power-bi
created: 2016-10-24T06:02:07.0000000Z
authors: []

---

When you run into a wall in Power BI and feel like you've exhausted the out of the box functionality, that when it's time to investigate what a bit of DAX can do for you. 
 
There are 2 different things you can do with DAX, create a Measure or a Calculated Column.

Calculated columns:

- Stored in the database
- Often used to filter/group data




Measures:



- Computed on aggregates of values
- Computed at query time
- Often used to give a numerical metric





GroupingColumn = if(value&lt;x, small, if(value&lt;y, medium, large))
Figure - Good Example: Nested if statements are a great way to split up your data into groups
