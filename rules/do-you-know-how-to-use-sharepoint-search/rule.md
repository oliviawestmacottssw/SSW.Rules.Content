---
type: rule
title: Do you know how to use SharePoint search?
uri: do-you-know-how-to-use-sharepoint-search
created: 2015-01-20T12:18:03.0000000Z
authors:
- id: 36
  title: Daniel Šmon
- id: 1
  title: Adam Cogan

---

 ​SharePoint search is a powerful tool for discovering information. Here are some tips to make sure you are getting the most from it. There are two things to consider regarding SharePoint search; firstly, how you save information to SharePoint to be more easily discoverable; secondly, how to perform searches within SharePoint. ​ 
### Tips for saving documents to be more discoverable

**When naming documents, use hyphens to separate words**

MonthlyReport.docx

Bad Example: File name doesn't contain any separators between words.

A file name without spaces means that the SharePoint doesn't know where one word ends and the other one begins. This means that searching for 'monthly' or 'report' would **not** find this document.



Monthly Report.docx

Bad Example: File name uses a space to separate words.

As far as SharePoint search goes, this is actually a usable option. What makes spaces less-preferable is the fact that the URL to this document will have those spaces escaped with the sequence %20. E.g. [https://sharepoint/site/library/Monthly%2 0 Report.docx](/Pages/Do-you-know-how-to-use-SharePoint-search.aspx). URLs with escaped spaces are longer and less human-readable.



Monthly\_Report.docx

Bad Example: File name uses an underscore to separate words.

As far as SharePoint search goes, an underscore is only a valid word separator in SharePoint Standard or Enterprise, from 2010 onwards. Underscores are not valid word separators for search in SharePoint foundation. Also, sometimes underscores are less visible to users, for example, when a hyperlink is underlined. When reading a hyperlink that is underlined, it is often possible for the user to be mistaken by thinking that the URL contains spaces instead of underscores. For these reasons it is best to avoid their use in file names and titles.



Monthly-Report.docx

Good Example: File name uses a hyphen to separate words.

A hyphen is the best choice, because it is understood both by humans and all versions of SharePoint search.



**Add relevant metadata where possible**

If a document library is configured with metadata fields, add as much relevant information as you can. Metadata is more highly regarded by search than the contents within documents, so by adding relevant terms to a documents metadata, you will almost certainly have a positive effect on the relevance of search results.



**Use descriptive file names and titles**

The file name and title is regarded more highly by search than the content within documents. Also, the title or file name is what is displayed in the search results, so by making it descriptive, you are making it easier for people who perform searches to identify the purpose of your document.

### Tips for performing searches

**Use Boolean OR and AND operators**

Similar to Google and Bing, you can use OR and AND Boolean operators. E.g. "sharepoint AND search".

Note: OR and AND must be capitalized, however case is irrelevant for actual search terms.



**Use an ** [**asterisk (\*)**](http&#58;//en.wikipedia.org/wiki/Asterisk) **wildcard for partial matches**

This can be useful if you know that certain words are used together, e.g. Fire\* will return results for FireBootCamp.

Note: Because of word stemming which is enabled by default in SharePoint 2013, you do not need to use wildcards to find variations on words. For example, searching for "computer" will return results that contain "computers", so you do not need to search for "computer\*".



**Use double quotes to find specific phrases**

E.g. search for "social media" to make sure you get results for social media, as opposed to results that simply contain the words "social" and "media" in the same document.



**Search a specific property if you are familiar with the structure of the metadata in the content you're searching**

You can restrict your searches to a property with the syntax &lt;property&gt;:&lt;search term&gt;. E.g. to search the filename field for the term "report", you would use "filename:report".




 
Good Example: Search on the SSW Intranet. 

