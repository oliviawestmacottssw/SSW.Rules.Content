---
type: rule
title: Do you check if your website is running?
uri: do-you-check-if-your-website-is-running
created: 2016-08-22T17:41:00.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

If you want to know your website is working or not, you need to add a ping check to the machine also an HTTP Content Scan to the website in WhatsUp. We use WhatsUp to do real-time monitoring.
Follow these steps to check your website in WhatsUp: 
1. Add your website as a new device.  
![ New device](running1.GIF) 

2. Ping monitor is added automatically.  
![ Ping monitor](running2.GIF) 

3. Add an HTTP Content Scan monitor.  
![ HTTP Content Scan](running3.GIF) 

4. Edit the scan script. In the script, you can see 2 keywords "Send" and "Expect".
"Send" expression is an  HTTP request to your website.
"Expect" expression is a regular expression to check the key word in response from your website.
  
![ Edit scan script](running4.GIF) 

5. Add the monitor to your device.  
![ Add monitor Once a device is down or up, a WhatsUp action will tell SQL Reporting Services to send out a notification report. ](running5.GIF) 

Our report looks like this:  
![ Website doesn't work](running6.GIF) 

 
![ Website works](running7.GIF)
