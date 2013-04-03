---
type: rule
title: Bounces - Do you know what to do with bounced email?
uri: bounces---do-you-know-what-to-do-with-bounced-email
created: 2011-08-25T19:54:59.0000000Z
authors: []

---

 Having people report bounce back emails is frustrating and time consuming. The first thing to try when you get a report is to check that your mail server isn’t on a spam blacklist. An easy way to check this is via [MX Toolbox](http&#58;//mxtoolbox.com/). ![Enter the domain to check](/PublishingImages/MXToolbox-1.jpg) Figure: Enter the domain to check ![Then select Blacklist Check](/PublishingImages/MXToolbox-2.jpg) Figure: Then select "Blacklist Check" ![not blacklisted](/PublishingImages/MXToolbox-3.jpg) Figure: Getting a zero is good, so you know that you are not blacklisted… so Step 1 is good 
Next step check that you have primary and secondary (and even better tertiary) MX records setup and working.
![SMTP test](/PublishingImages/MXToolbox-4.jpg) Figure: Seeing at least 2 MX records is good... Run an SMTP Test to test mail servers. So Step 2 is good 
If success on both steps the error is most likely on the senders side. Send them the an email to check their mail settings.


Dear xxx

As per this rule on bounced emails http://rules.ssw.com.au/Communication/RulesToBetterEmail/Pages/Do-you-know-what-to-do-with-bounced-email.aspx

- I have checked Step 1 – it is good
- I have checked Step 2 – it is good
    The problem is likely your end


Figure: What to send the person 
