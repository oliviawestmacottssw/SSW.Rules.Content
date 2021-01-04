---
type: rule
archivedreason: 
title: Authentication - Do you have a 'Forgot my password' link?
guid: 07cac45a-80f4-4acb-a9df-7408987536c0
uri: authentication---do-you-have-a-forgot-my-password-link
created: 2014-12-11T20:10:16.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
- title: Duncan Hunter
  url: https://ssw.com.au/people/duncan-hunter
related: []
redirects: []

---

It's easy and common for users to forget their passwords, the vital key which grants                     them access to the services they are eligible for. To cater for this instance, it                     is important to have a 'Forgot my password' link on the sign in page.

<!--endintro-->
<dl class="badImage">&lt;dt&gt; 
      <img src="bad.png" alt="bad.png">
   &lt;/dt&gt;<dd>Figure: Bad example - what will happen for the poor user that forgot his password?</dd></dl><dl class="goodImage">&lt;dt&gt;
      <img src="good.png" alt="good.png">
   &lt;/dt&gt;<dd> Figure: Good example - users have an option if they forget their password</dd></dl><dl class="goodImage">&lt;dt&gt;
      <img src="reset example.png" alt="reset example.png">
   &lt;/dt&gt;<dd> Figure: Good example - users can enter their email to get a new password</dd></dl>
### Do you avoid a username enumeration attack?


This practice also opens up the risk of "username enumeration" where an entire collection of usernames or email addresses can be validated for existence on the website simply by batching requests and looking at the responses. You can read more on     [Troy Hunt's blog post](http://www.troyhunt.com/2012/05/everything-you-ever-wanted-to-know.html). You should always aim to not disclose if a user is registered with your site or not.
<dl class="badImage">&lt;dt&gt;
      <img src="2016-01-05_15-20-06.png" alt="2016-01-05_15-20-06.png">
   &lt;/dt&gt;<dd>Figure: Bad example - Displaying information that a user does not exist?</dd></dl><dl class="goodImage">&lt;dt&gt;
      <img src="demo.png" alt="demo.png">
   &lt;/dt&gt;<dd>Good example - You should always aim to not disclose if a user is registered with your site or not<br></dd></dl>
