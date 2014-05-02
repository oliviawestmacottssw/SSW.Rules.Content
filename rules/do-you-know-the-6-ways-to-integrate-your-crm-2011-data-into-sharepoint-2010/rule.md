---
type: rule
title: Do you know the 6 ways to integrate your CRM 2011 data into SharePoint 2010?
uri: do-you-know-the-6-ways-to-integrate-your-crm-2011-data-into-sharepoint-2010
created: 2011-08-24T03:52:23.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 24
  title: Adam Stephensen
- id: 9
  title: William Yin

---

 
You have data in CRM 2011, so how do you see it in SharePoint? The data that is stored in CRM entities should be available in SharePoint so users can find and use the data in areas such as:

- SharePoint search

- SharePoint reporting (if you are using SQL Reporting Services in integrated mode)

There are many ways to get to this data, let's go through them:
 

### OPTION 1: SharePoint BCS A​​dapter (provided by the CRM Team) RECOMMENDED

This BCS Adapter for CRM 2011 is from the CRM team (It does all of the BCS work for you by interrogating the CRM metadata service).

Summary: SharePoint BCS -&gt; Pre-built Adapter (.NET Assembly) -&gt; CRM web services - &gt; CRM database


| Pros | Cons |
| --- | --- |
| ![clip_image002\[8\]](/PublishingImages/correct.gif "clip_image002[8]")Read/Write<br><br>![clip_image002\[9\]](/PublishingImages/correct.gif "clip_image002[9]")Minimal coding<br><br>![clip_image002\[10\]](/PublishingImages/correct.gif "clip_image002[10]")Easiest to implement<br><br>![clip_image002\[11\]](/PublishingImages/correct.gif "clip_image002[11]")The likely way forward (Best Practice as Microsoft) | ![clip_image004\[13\]](/PublishingImages/wrong.gif "clip_image004[13]")Needs to be deployed and published to the web server.<br><br>![clip_image004\[14\]](/PublishingImages/wrong.gif "clip_image004[14]")Less performance than SQL filter views directly<br><br>![clip_image004\[15\]](/PublishingImages/wrong.gif "clip_image004[15]")Only recently released. |


[![clip_image010](/PublishingImages/figure5.jpg "clip_image010")](/PublishingImages/figure5.jpg) 
**Figure: CRM data available in SharePoint**

**More information:**

Download from Microsoft

Read "*Connecting to CRM Online 2011 with SharePoint 2010 Business Connectivity Services*"

Run tool to generate the XML mapping (.BDCM)

This solution uses a BCS Connector – a .NET Assembly responsible for mapping external data into a form usable by SharePoint. This component is loaded and hosted within SharePoint 2010, and communicates with CRM via the CRM Proxy Service.




### Option 2: SQL Server Filtered Views


CRM recommends that you \*don't\* read from the Tables, so they provide SQL Views for this purpose.

Summary: SharePoint BCS -&gt; CRM database


| Pros | Cons |
| --- | --- |
| ![clip_image002](/PublishingImages/correct.gif "clip_image002")Easiest<br><br>![clip_image002\[1\]](/PublishingImages/correct.gif "clip_image002[1]")Best performance<br><br>![clip_image002\[2\]](/PublishingImages/correct.gif "clip_image002[2]")Codeless | ![clip_image004](/PublishingImages/wrong.gif "clip_image004")Read-only<br><br>![clip_image004\[1\]](/PublishingImages/wrong.gif "clip_image004[1]")Not available for hosted CRM<br><br>![clip_image004\[2\]](/PublishingImages/wrong.gif "clip_image004[2]") Security issues as you are exposing the view. |


Filtered Views in Microsoft CRM provide access to the data available that supports providing picklist name and id values (lookup tables).

**More information: **

If you only want read-only for CRM on-premises data for SharePoint users, this solution is fine. You create the External Content Type directly against the Filtered Views in the CRM database.

[http://msdn.microsoft.com/en-us/library/gg328467.aspx](http&#58;//msdn.microsoft.com/en-us/library/gg328467.aspx)

![clip_image005](/PublishingImages/figure1.jpg "clip_image005")

**Figure: The result of “SELECT \* FROM FilteredCtx\_Project”. Use Office SharePoint Designer to hook this up.**

### 


### OPTION 3​: Web Services

CRM provides web services.

Summary: SharePoint BCS -&gt; Code calling CRM web services - &gt; CRM database​


| Pros | Cons |
| --- | --- |
| ![clip_image002\[3\]](/PublishingImages/correct.gif "clip_image002[3]")Read/Write | ![clip_image004\[3\]](/PublishingImages/wrong.gif "clip_image004[3]")Needs lots of code and test work.<br><br>![clip_image004\[4\]](/PublishingImages/wrong.gif "clip_image004[4]")Needs to be deployed and published to the web server.<br><br>![clip_image004\[5\]](/PublishingImages/wrong.gif "clip_image004[5]")Less performance than SQL filter views directly #1 |


#1 Note: Performance could be improved by making the reads from the views and the writes through the web service

**More information:  **

1. Use BCS in VS 2010

2. Write code that calls the CRM web services (that access the CRM data)

3. Test

4. Deploy

### 


### OPTION 4​​: Expose OData from CRM as RSS

The CRM 2011 OData Query Designer can be used to build queries to expose the data from CRM as RSS


| Pros | Cons |
| --- | --- |
| ![clip_image002\[4\]](/PublishingImages/correct.gif "clip_image002[4]")Easy configuration | ![clip_image004\[6\]](/PublishingImages/wrong.gif "clip_image004[6]")50 records limit. Need to page through the results.<br><br>![clip_image004\[7\]](/PublishingImages/wrong.gif "clip_image004[7]")Possible issues with firewalls and proxies because it uses Integrated Security for authentication.<br><br>![clip_image004\[8\]](/PublishingImages/wrong.gif "clip_image004[8]")Read-Only<br><br>![clip_image004\[9\]](/PublishingImages/wrong.gif "clip_image004[9]")No easy way to consume |


**
**Note: You can really only call the OData endpoint from an application that already has an authentication cookie with the CRM server. 
i.e. you can't impersonate and call it like you can the standard WCF endpoints 
So it is really only suited to calling from Silverlight and JavaScript web resources that are delivered inside CRM (because they have the cookie)

**More information: **

The first step is to expose the data:

1. Install [http://crm2011odatatool.codeplex.com](http&#58;//crm2011odatatool.codeplex.com/)

2. Make a query

![clip_image006](/PublishingImages/figure2.jpg "clip_image006")

**Figure: Designing a query**

3. See the data

![/SoftwareDevelopment/rulestobettercrm/PublishingImages/figure3.jpg](/PublishingImages/figure3.jpg "clip_image007")

**                Figure: See the data - RSS source for xtc\_countrySet**

The second step (and the problem) is consuming the data

**![clip_image009](/PublishingImages/figure4.jpg "clip_image009")**

**Figure: BCS has no option to consume RSS data. Please Microsoft SharePoint Team, we need a new 'Data Source Type' = OData**

In summary, CRM 2011 can exposes OData, but SharePoint 2010 BCS doesn't consume OData.

The 3 options to consume the OData/RSS data:

· Consume the OData by SQL Server, via TSQL ???    Then use BCS to call SQL Server. 
Summary: SharePoint BCS -&gt; DataSourceType: SQL Server -&gt; OData- &gt; CRM database

You would need to be crazy to go down this route [http://www.vishalseth.com/post/2009/12/22/Call-a-webservice-from-TSQL-(Stored-Procedure)-using-MSXML.aspx](http&#58;//www.vishalseth.com/post/2009/12/22/Call-a-webservice-from-TSQL-%28Stored-Procedure%29-using-MSXML.aspx)

· Consume the OData by a BCS adapter + code calling web services (same story as above). 
Summary: SharePoint BCS -&gt; code calling OData- &gt; CRM database

· Consume the RSS by "SharePoint RSS view web part" directly. 
Summary: SharePoint RSS view web part -&gt; OData- &gt; CRM database 
(not recommended as it could not be used in "SharePoint Search")

So OData is all things horrible because it is hard to eat :-(

### 


### OPTION 5: BizTalk​

Biztalk is built for mapping systems together, unfortunately this solution is only considered for large enterprises.

Summary: SharePoint BCS -&gt; BizTalk Database - &gt; CRM database


| Pros | Cons |
| --- | --- |
| ![clip_image002\[5\]](/PublishingImages/correct.gif "clip_image002[5]")Read/Write<br><br>![clip_image002\[6\]](/PublishingImages/correct.gif "clip_image002[6]")The BizTalk data centre can also provide data for any system.<br><br>![clip_image002\[7\]](/PublishingImages/correct.gif "clip_image002[7]")Requires little code if users already have BizTalk | ![clip_image004\[10\]](/PublishingImages/wrong.gif "clip_image004[10]")BizTalk :-)<br><br>![clip_image004\[11\]](/PublishingImages/wrong.gif "clip_image004[11]")Deployment - Needs external work to deploy BizTalk server.<br><br>![clip_image004\[12\]](/PublishingImages/wrong.gif "clip_image004[12]")Licence Cost |


**
**



### Option 6: OData 3rd Party solutions (doesn't exist)

Today SharePoint 2010 exposes lists and document libraries as OData, but does not natively consume OData.

What does this mean?

- CRM 2011 exposes it data as OData, but cannot consume OData

- SharePoint 2010 exposes it data as OData, but cannot consume OData

....and there are no 3rd party solutions to solve this...

