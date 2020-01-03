---
type: rule
archivedreason: 
title: Data - Dates - Do you know DateTime fields must be converted to universal time?
guid: 96636654-80f5-46c9-adb0-a8ddfe98e7e3
uri: data-dates-do-you-know-datetime-fields-must-be-converted-to-universal-time
created: 2019-11-25T19:54:23.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
- title: Christian Morford-Waite
  url: https://ssw.com.au/people/christian-morford-waite
related: []
redirects: []

---


<p>​Any DateTime fields must be converted to universal time from the application to the stored procedures when storing data into the database.<br></p><p>When retrieving data from the database it must be converted back to the local time of the user.<br>That way you get an accurate representation of&#160;the time someone entered data into the database (i.e. the DateUpdated field).</p><p>The exception to this rule, however, is for already existing databases that deal with DateTime as part of their queries.<br>e.g. SSW Time PRO.NET is an application that allows employees to enter their timesheet. The table used for storing this information has an important field that has a DateTime data type.<br>This cannot be converted to UTC in the database because that would mean&#58;<br>&#160;</p><ol><li>Converting every single entry since entries began being stored (in SSW's case since 1996) to keep information consistent;</li><li>Other separate applications currently using the timesheet information in the database for reporting will also have to be entirely modified.</li></ol><p>Currently there will be an issue if for example someone from the US (Pacific time) has 19 hours difference between her local time and our servers.<br><br></p>
<br><excerpt class='endintro'></excerpt><br>
<p><strong>​​​Example&#58;</strong>&#160;Sally in the US enters a timesheet for the 21/04/05. (which will default to have a time of 12&#58;00&#58;00 AM since the time was not specified)<br>Our servers will store it as 21/04/05 19&#58;00&#58;00 in other words 21/04/05 07&#58;00&#58;00 PM because the .NET Framework will automatically convert the time accordingly for our Web Service.<br>Therefore our servers have to take the Date component of the DateTime and add the Time component as 12&#58;00&#58;00 AM to make it stored in our local time format.<br></p><p class="ssw15-rteElement-CodeArea">[WebMethod] <br>public double GetDateDifference(DateTime dateRemote) <br>&#123; <br>DateTime dateLocal = dateRemote.Date; <br>​​return (dateRemote.TimeOfDay.TotalHours - <br>​​dateLocal.TimeOfDay.TotalHours); <br>​&#125;</p><p><strong>Figure&#58; When dateRemote is passed in from the remote machine, .Net Framework will have already converted it to the UTC equivalent for the local server (i.e. the necessary hours would have been added to cater for the local server time).</strong></p><p>In the above code snippet, the .Date property would cut off the Time portion of the DateTime variable and set the Time portion to &quot;12&#58;00&#58;00 AM&quot; as default.</p><p>This is for applications we currently have that&#58;</p><ol><li>Consider the DateTime component integral for the implementation of the application</li><li>That will be used world wide.</li></ol><p><br></p>


