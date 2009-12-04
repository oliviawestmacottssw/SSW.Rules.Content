---
type: rule
archivedreason: 
title: Do you know changes on Datetime in .NET 2.0 and .NET 1.1/1.0
guid: aae59cde-200b-4d55-90b1-ed0db45d32af
uri: do-you-know-changes-on-datetime-in-net-20-and-net-11-10
created: 2009-05-08T08:37:20.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
- title: Ryan Tee
  url: https://ssw.com.au/people/ryan-tee
related: []
redirects: []

---


This field should not be null (Remove me when you edit this field).
<br><excerpt class='endintro'></excerpt><br>
<br>
<dl class="goodCode">
<dt style="width&#58;91.71%;height&#58;68px;"><pre>DataSet returnedResult = webserviceObj.GetByDateCreatedAndEmpID(DateTime.<br>Now,'JZ');                            </pre></dt></dl><b>Figure&#58; front end code in .NET v1.1 (front end time zone&#58; GTM+8)</b><br>
<dl class="goodCode">
<dt style="width&#58;92.48%;height&#58;168px;"><pre>[WebMethod] public DataSet GetByDateCreatedAndEmpID(DateTime DateCreated, String                                <br>EmpID)                                <br>&#123;<br>     EmpTimeDayDataSet ds = new EmpTimeDayDataSet();                                <br>     m_EmpTimeDayAdapter.FillByDateCreatedAndEmpID(ds, DateCreated.Date, EmpID);                                <br>     return ds;<br>&#125;                            </pre></dt></dl>
<p><b>Figure&#58; web service method (web service server time zone&#58; GTM+10)</b></p>
<p>When front end calls this web method with the value of current local time (14/01/2006 11&#58;00&#58;00 PM GTM+8) for parameter 'DateCreated', it expects a returned result for date 14/01/2006, while the service end returns data of 15/01/2006, because 14/01/2006 11&#58;00&#58;00 PM (GTM+8) would be adjusted to be 15/01/2006 01&#58;00&#58;00 AM at the web service server (GTM+10) </p>
<p>In v1.1/v1.0 you have no way to control this serializing/deserializing behaviour on DateTime. In v2.0 with the new notion DateTimeKind you can get a workaround for above example, </p>
<dl class="goodCode">
<dt style="width&#58;92.32%;height&#58;89px;"><pre>Datetime unspecifiedTime = DateTime.SpecifyKind(DateTime.Now,DateTimeKind.<br>Unspecified);                                <br>DataSet returnedResult = webservceObj.serviceObj.GetByDateCreatedAndEmpID,<br>(unspecifiedTime,'JZ');                            </pre></dt></dl>
<p><b>Figure&#58; front end code in .NET v2.0 (front end time zone&#58; GTM+8)</b></p>
<p>In this way, the server end will always get a datetime value of 14/01/2006 11&#58;00&#58;00 without GTM offset and return what front end expects</p>


