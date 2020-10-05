---
type: rule
title: Schema - Do you only use Unicode datatypes (nchar, nvarchar and ntext) in special circumstances?
uri: schema---do-you-only-use-unicode-datatypes-nchar-nvarchar-and-ntext-in-special-circumstances
created: 2019-11-05T22:41:29.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

Columns defined using the nchar and nvarchar datatypes can store any character defined by the Unicode Standard, which includes all of the characters defined in the various English and Non-English character sets. These datatypes take twice as much storage space per characters as non-Unicode data types.
 
​It is not the disk space costs that are the concern. It is the 8060 limit, please refer to [Maximum Capacity Specifications for SQL Server​](https&#58;//docs.microsoft.com/en-us/sql/sql-server/maximum-capacity-specifications-for-sql-server?redirectedfrom=MSDN&amp;view=sql-server-ver15) for details.

​If your database stores only English characters, this is a waste of space. Don't use Unicode double-byte datatypes such as nchar and nvarchar unless you are doing multilingual applications.

If you need to store more that 255 Characters, use Varchar(max) or nvarchar(max).
