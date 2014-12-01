---
type: rule
title: Do you remember the user's last settings?
uri: do-you-remember-the-users-last-settings
created: 2014-12-01T04:05:27.0000000Z
authors: []

---

 
The user's last settings should be saved and should be selected as the Default the                     next time a form is opened in many instances. For example:
 
- Login forms - the last login name should be the Default selected and the cursor should be in the password box. <br>      <dl class="badImage"><dt> 
            <img border="0" alt="SSW Time PRO .NET - Login" src="http&#58;//www.ssw.com.au/ssw/Standards/Rules/Images/BadFormLogin.jpg" style="margin&#58;5px;width&#58;342px;">
         </dt><dd> Figure&#58; Bad Example - Last Username is not saved</dd></dl><dl class="goodImage"><dt> 
            <img border="0" alt="SSW Time PRO .NET - Login" src="http&#58;//www.ssw.com.au/ssw/Standards/Rules/Images/GoodFormLogin.jpg" style="margin&#58;5px;width&#58;342px;">
         </dt><dd> Figure&#58; Good Example - Last Username is saved</dd></dl>
- Report criteria forms - e.g. date start and date end fields should be automatically populated


How do I store the settings?

- .NET: Use the <br>      [Configuration Block](/do-you-use-configuration-management-application-block) to store the settings.
- Access: Use a local table called 'Control' with one record.


