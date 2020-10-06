---
type: rule
title: Do you use a regular expression to validate an email address?
uri: do-you-use-a-regular-expression-to-validate-an-email-address
created: 2018-04-25T23:15:46.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

A regex is the best way to verify an email address.
 
public bool IsValidEmail(string email)
{
 // Return true if it is in valid email format.
 if (email.IndexOf("@") &lt;= 0) return false; 
 if (email.EndWith("@")) return false; 
 if (email.IndexOf(".") &lt;= 0) return false; 
 if ( ... 
}
Figure: Bad example of verify email address

public bool IsValidEmail(string email) 
{ 
 // Return true if it is in valid email format.
 return System.Text.RegularExpressions.Regex.IsMatch( email, 
 @"^([\w-\.]+)@(([[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.)|(([\w-]+\.)+))([a-zA-Z]{2,4}|[0-9]{1,3})(\]?)$";
}
Figure: Good example of verify email address
