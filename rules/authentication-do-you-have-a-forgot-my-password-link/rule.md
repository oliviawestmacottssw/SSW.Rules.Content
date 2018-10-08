---
type: rule
archivedreason: 
title: Authentication - Do you have a 'Forgot my password' link?
guid: 07cac45a-80f4-4acb-a9df-7408987536c0
uri: authentication-do-you-have-a-forgot-my-password-link
created: 2014-12-11T20:10:16.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
- title: Duncan Hunter
  url: https://ssw.com.au/people/duncan-hunter
related: []
redirects: []

---


<p>It's easy and common for users to forget their passwords, the vital key which grants
                    them access to the services they are eligible for. To cater for this instance, it
                    is important to have a 'Forgot my password' link on the sign in page.​<br></p>
<br><excerpt class='endintro'></excerpt><br>
<dl class="badImage"><dt> <img src="/SiteAssets/authentication-do-you-have-a-forgot-my-password-link/bad.png" alt="bad.png" /></dt><dd>Figure&#58; Bad example - what will happen for the poor user that forgot his password?</dd></dl><dl class="goodImage"><dt><img src="/SiteAssets/authentication-do-you-have-a-forgot-my-password-link/good.png" alt="good.png" /></dt><dd> Figure&#58; Good example - users have an option if they forget their password</dd></dl><dl class="goodImage"><dt><img src="/SiteAssets/authentication-do-you-have-a-forgot-my-password-link/reset%20example.png" alt="reset example.png" /></dt><dd> Figure&#58; Good example - users can enter their email to get a new password</dd></dl><h3>​Do you avoid a&#160;username enumeration attack?<br></h3><p>This practice also opens up the risk of &quot;username enumeration&quot; where an entire collection of usernames or email addresses can be validated for existence on the website simply by batching requests and looking at the responses. You can read more on <a href="http&#58;//www.troyhunt.com/2012/05/everything-you-ever-wanted-to-know.html">Troy Hunt's blog post</a>. You should always aim to not disclose if a user is registered with your site or not.</p><dl class="badImage"><dt><img src="/SiteAssets/authentication-do-you-have-a-forgot-my-password-link/2016-01-05_15-20-06.png" alt="2016-01-05_15-20-06.png" /></dt><dd>Figure&#58; Bad example - Displaying information that a user does not exist?</dd></dl><dl class="badImage"><dt><img src="/SiteAssets/authentication-do-you-have-a-forgot-my-password-link/demo.png" alt="demo.png" /></dt><dd>Figure&#58; Bad example - what will happen for the poor user that forgot his password? <br></dd></dl>


