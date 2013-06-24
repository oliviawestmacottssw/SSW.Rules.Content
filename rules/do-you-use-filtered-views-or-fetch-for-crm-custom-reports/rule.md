---
type: rule
title: Do you use Filtered Views or Fetch for CRM Custom Reports?
uri: do-you-use-filtered-views-or-fetch-for-crm-custom-reports
created: 2012-12-10T18:40:08.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 32
  title: Mehmet Ozdemir

---

 
Directly querying the table bypasses the security and filtering of MSCRM as well           as not being supported by Microsoft. This​ is not the correct method for reports           to be written.           
           The correct filtered views can be found under the Views section of the CRM database           and these are the Views that should always be used to design SQL Reporting Services           reports.
 ![When developing reports don't go against the base tables - instead use the filtered views of Microsoft CRM 3.0](/SoftwareDevelopment/RulesToBetterCRMForDevelopers/PublishingImages/CRM_FilteredView.jpg)            Figure: When developing reports don't go against the base tables - instead use the<br>            filtered views of Microsoft CRM 4
In CRM 2011 using Filtered Views is enforced with data connector, direct access to tables and other views will be denied.

