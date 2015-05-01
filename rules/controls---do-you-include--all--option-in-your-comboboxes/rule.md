---
type: rule
title: Controls - Do you include '-All-' option in your ComboBoxes?
uri: controls---do-you-include--all--option-in-your-comboboxes
created: 2012-11-27T08:38:56.0000000Z
authors: []

---

 
ComboBoxes are often used for filtering data. It is best to have an '-All-' option to give your user chances to select all data.




It is important to understand the idea of **visual text**. In a list you could see either:

- -None- or
- No activity assigned


They both have the same meaning, but the first one is immediately visible whereas the second one must be read.
 


If the ID column in your database is a string data type, it ​is useful to add a constraint to limit the types of characters that it can contain. Adding a constraint can make it simpler to build your front-end, as you won't need to worry about encoding or escaping to handle special characters.



In SQL Server, you can add a check constraint that limits your column to alphanumeric characters, a hyphen, or underscore using the following T-SQL:

ALTER TABLE [TableName] ADD CONSTRAINT CK\_String\_Identifier​
    CHECK ([StringIdColumn] NOT LIKE'%[^a-zA-Z0-9\_\-]%')​






![ComboBox without All](http&#58;//www.ssw.com.au/ssw/Standards/Rules/Images/Combo-ALL-1.jpg)
<dl class="badImage"><dd>Figure&#58; Bad Example - No '-All-' option so the user cannot select all data</dd></dl><dl class="goodImage"><dt><img alt="ComboBox without All" src="http&#58;//www.ssw.com.au/ssw/Standards/Rules/Images/Combo-ALL-2.jpg"></dt>
<dd>Figure&#58; Good Example - Having an '-All-' option gives a user a chance to select all data</dd></dl>
Also, keep it simple!
<dl class="badImage"><dt><img alt="All Stores" src="http&#58;//www.ssw.com.au/ssw/Standards/Rules/Images/SelectAllBad.jpg"></dt>
<dd>Figure&#58; Bad Example - '-All Stores-' isn't needed</dd></dl><dl class="goodImage"><dt><img alt="All" src="http&#58;//www.ssw.com.au/ssw/Standards/Rules/Images/SelectAllGood.jpg"></dt>
<dd>Figure&#58; Good Example - Keep it as a simple '-All-'</dd></dl><dl class="goodImage"><dt><img alt="All" src="http&#58;//www.ssw.com.au/ssw/Standards/Rules/Images/SelectAllVGood.gif"></dt>
<dd>Figure&#58; Good Example - Keeping it simple makes it easy to spot (that there is no filter) when you have multiple fields.</dd></dl>
Read our rule on [Always make sure the dimensions All Captions = All](http&#58;//www.ssw.com.au/ssw/Standards/Rules/RulesToBetterBusinessIntelligence.aspx#AllDimensionsTag).






