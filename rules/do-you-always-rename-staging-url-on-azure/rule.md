---
type: rule
title: Do you always rename staging Url on Azure?
uri: do-you-always-rename-staging-url-on-azure
created: 2015-03-08T23:23:53.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 47
  title: Stanley Sidik
- id: 43
  title: Michael Demarco
- id: 42
  title: Shigemi Matsumoto

---

 
Do you feel pain testing your code on Azure staging site? I did because the Url wasn't easy to remember. Follow this rule to increase your productivity.


 

| Default Azure Url naming with staged publishing:<br><ul><li><span style="line-height&#58;20px;">Production web site&#58; <strong>sugarlearning.com</strong> (or sugarlearning.azurewebsites.net)</span></li><li><span style="line-height&#58;20px;">Staging web site&#58; <strong><strong>sugarlearning<span style="color&#58;#ff0066;">-staging</span>.azurewebsites.net</strong></strong></span></li></ul> |
| --- |

Bad e​​​​xample: Site using the default Url (hard to remember!!)

| Add a CName to resolve default Url like this:<br><ul><li><span style="line-height&#58;20px;">Production web site&#58; <strong>sugarlearning.com</strong> (or sugarlearning.azurewebsites.net)</span></li><li><span style="line-height&#58;20px;">Staging web site&#58; <strong><font color="#ff0066">staging</font></strong>.<strong>sugarlearning.com </strong>(or&#160;sugarlearning-staging.azurewebsites.net)</span></li></ul> |
| --- |

​Good ​example: Staging Url having production Url with "staging." prefix
