---
type: rule
title: Do you use the right service in SharePoint 2013
uri: do-you-use-the-right-service-in-sharepoint-2013
created: 2013-08-27T06:31:48.0000000Z
authors:
- id: 35
  title: Brian Farnhill
- id: 8
  title: John Liu

---

In SharePoint 2010, you can use SharePoint service  **/\_vti\_bin/listdata.svc** to access data in SharePoint list, but in SharePoint 2013,  **/\_vti\_bin/listdata.svc** has been officially deprecated.


   The new service in SharePoint 2013 is  **http://server/site/\_api/web/lists/getbytitle('listname')** 
 **
**  
Read more about it: 

[http://msdn.microsoft.com/en-us/library/office/dn292556.aspx](http&#58;//msdn.microsoft.com/en-us/library/office/dn292556.aspx)
