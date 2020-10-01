---
type: rule
title: Do you force SSL on sensitive methods like “Login” or “Register”?
uri: do-you-force-ssl-on-sensitive-methods-like-login-or-register
created: 2013-03-07T18:21:09.0000000Z
authors:
- id: 23
  title: Damian Brady

---

Any sensitive data that is sent over the wire must be protected using a secure transport such as HTTPS.  MVC (version 2, Preview 2 or higher) allows you to specify that HTTPS is required for an action.  It’s important that the GET method is secure as well as the POST method to avoid people sending sensitive form data over the wire.
 

```
public ActionResult Register()
{
   return View();
}
```

Figure: Bad Example – The Register method isn’t secure

```
[RequireHttps]
public ActionResult Login()
{
   return View();
}
```

Figure: Good Example – The Login method is protected by HTTPS
