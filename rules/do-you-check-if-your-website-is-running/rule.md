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
​Follow these steps to check your website in WhatsUp: 
1. Add your website as a new device.  ![running1.GIF](running1.GIF) Figure: New device
2. Ping monitor is added automatically.  ![running2.GIF](running2.GIF) Figure: Ping monitor
3. Add an HTTP Content Scan monitor.  ![running3.GIF](running3.GIF) Figure: HTTP Content Scan
4. Edit the scan script. In the script, you can see 2 keywords "Send" and "Expect".
"Send" expression is an  HTTP request to your website.
"Expect" expression is a regular expression to check the key word in response from your website.
  ![running4.GIF](running4.GIF) Figure: Edit scan script
5. Add the monitor to your device.  ![running5.GIF](running5.GIF) Figure: Add monitor Once a device is down or up, a WhatsUp action will tell SQL Reporting Services to send out a notification report. 
Our report looks like this:  ![running6.GIF](running6.GIF) Figure: Website doesn't work
 ![running7.GIF](running7.GIF) Figure: Website works


