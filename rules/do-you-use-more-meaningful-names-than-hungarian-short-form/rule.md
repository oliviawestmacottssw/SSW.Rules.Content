---
type: rule
title: Do you use more meaningful names than Hungarian short form?
uri: do-you-use-more-meaningful-names-than-hungarian-short-form
created: 2009-05-05T07:29:18.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 17
  title: Ryan Tee

---

 This field should not be null (Remove me when you edit this field). 

```
//Bad Code
                          DateTime dt = new DateTime.Now();

                          DataSet ds = new DataSet();

                          // It could be confused with Date time.

                          DataTable dt = ds.Tables[0];
```

Bad code - Without meaningful name. 

```
//Good Code
                     DateTime currentDateTime = new DateTime.Now();

                     DataSet employmentDataSet = new DataSet();

                     DataTable ContactDetailsDataTable = ds.Tables[0];
```

Good code - With meaningful name. 
[More information on naming convention](http&#58;//www.ssw.com.au/ssw/Standards/DeveloperDotNet/DotNetStandard_ObjectNaming.aspx).




| We have a program called [SSW Code Auditor](http&#58;//www.ssw.com.au/ssw/CodeAuditor/Default.aspx) to check for this rule |
| --- |


