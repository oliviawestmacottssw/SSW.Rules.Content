---
type: rule
archivedreason: 
title: Do you use Group Policy to enable auditing of logon attempts​?
guid: 88f40e36-75c1-40ae-8884-f86859ae2568
uri: do-you-use-group-policy-to-enable-auditing-of-logon-attempts
created: 2019-07-24T20:57:45.0000000Z
authors:
- title: Steven Andrews
  url: https://ssw.com.au/people/steven-andrews
related: []
redirects:
- use-group-policy-to-enable-auditing-of-logon-attempts

---

It is important as a Network Administrator to know when and where failed login attempts are coming from. Through Group Policy you can enable "Audit logon events".

<!--endintro-->

1. Create a group policy called 'Logon Auditing Policy'
2. Right click on 'Logon Auditing Policy' and click on Edit to bring up Group Policy Management Editor
3. Select 'Audit account logon events' from Computer Configuration | Policies | Windows Settings | Local Policies | Audit Policy and set to Success, Failure
4. Select 'Audit logon events' from Computer Configuration | Policies | Windows Settings | Local Policies | Audit Policy and set to Success, Failure
<dl class="image"><dt>
            <img src="failed-login-1.png" alt="failed-login-1.png">
         </dt><dd>Figure: Select 'Audit logon events'<br></dd></dl>
5. Select 'Audit: Force audit policy...' from Computer Configuration | Policies | Windows Settings | Local Policies | Security Options and set to Enabled
<dl class="image"><dt>
            <img src="failed-login-2.png" alt="failed-login-2.png">
         </dt><dd>Figure: Select 'Audit: Force audit policy...'<br></dd></dl>

<dl class="image"><dt><img src="failed-login-3.png" alt="failed-login-3.png"></dt><dd>Figure: Successful and Failed login attempts will now appear in Event Viewer | Security</dd></dl>Now when you will have access to seeing success/failed login attempts on user accounts, these can then be captured and audited with your own internal process or a third party application such as Whats Up Gold, see: [Do you monitor failed login attempts?](/monitor-failed-login-attempts)
