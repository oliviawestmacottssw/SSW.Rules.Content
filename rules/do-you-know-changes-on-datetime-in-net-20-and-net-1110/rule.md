---
type: rule
title: Do you know changes on Datetime in .NET 2.0 and .NET 1.1/1.0
uri: do-you-know-changes-on-datetime-in-net-20-and-net-1110
created: 2009-05-08T08:37:20.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 17
  title: Ryan Tee

---

In v1.0 and v1.1 of .NET framework when serializing DateTime values with the XmlSerializer, the local time zone of machine would always been appended. And when deserializing on the receiving machine, DateTime values would be automatically adjusted based on time zone offset relative to the sender time zone. See below example:<br> 


```
DataSet returnedResult = webserviceObj.GetByDateCreatedAndEmpID(DateTime.Now,'JZ');
```

**Figure: front end code in .NET v1.1 (front end time zone: GTM+8)**


```
[WebMethod] public DataSet GetByDateCreatedAndEmpID(DateTime DateCreated, String                                EmpID)                                {     EmpTimeDayDataSet ds = new EmpTimeDayDataSet();                                     m_EmpTimeDayAdapter.FillByDateCreatedAndEmpID(ds, DateCreated.Date, EmpID);                                     return ds;}
```


**Figure: web service method (web service server time zone: GTM+10)**

When front end calls this web method with the value of current local time (14/01/2006 11:00:00 PM GTM+8) for parameter 'DateCreated', it expects a returned result for date 14/01/2006, while the service end returns data of 15/01/2006, because 14/01/2006 11:00:00 PM (GTM+8) would be adjusted to be 15/01/2006 01:00:00 AM at the web service server (GTM+10)

In v1.1/v1.0 you have no way to control this serializing/deserializing behaviour on DateTime. In v2.0 with the new notion DateTimeKind you can get a workaround for above example,


```
Datetime unspecifiedTime = DateTime.SpecifyKind(DateTime.Now,DateTimeKind.Unspecified);                                DataSet returnedResult = webservceObj.serviceObj.GetByDateCreatedAndEmpID,(unspecifiedTime,'JZ');
```


**Figure: front end code in .NET v2.0 (front end time zone: GTM+8)**

In this way, the server end will always get a datetime value of 14/01/2006 11:00:00 without GTM offset and return what front end expects
