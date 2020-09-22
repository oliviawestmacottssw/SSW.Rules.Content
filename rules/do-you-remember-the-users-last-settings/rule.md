---
type: rule
title: Do you remember the user's last settings?
uri: do-you-remember-the-users-last-settings
created: 2014-12-01T04:05:27.0000000Z
authors: []

---

 
The user's last settings should be saved and should be selected as the Default the                     next time a form is opened in many instances. For example:
 
- Login forms - the last login name should be the Default selected and the cursor should be in the password box. <br>      ![SSW Time PRO .NET - Login](../../assets/BadFormLogin.jpg) Figure: Bad Example - Last Username is not saved![SSW Time PRO .NET - Login](../../assets/GoodFormLogin.jpg) Figure: Good Example - Last Username is saved
- Report criteria forms - e.g. date start and date end fields should be automatically populated


How do I store the settings?

- .NET: Use the <br>      [Configuration Block](/do-you-use-configuration-management-application-block) to store the settings.
- Access: Use a local table called 'Control' with one record.


