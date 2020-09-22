---
type: rule
title: Printers - Do you make your Printers easy to find?
uri: printers---do-you-make-your-printers-easy-to-find
created: 2012-03-05T15:41:28.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

 
For PCs that are not in the domain, the printers won’t be automatically installed.

So you should add a DNS alias which maps \\printer to your print server.
![Add the printer via Connect](add-printer-via-connect.jpg)Figure: \\printer takes to this window, were you can "Add" the printer via Connect
Note: It is better to automate mappings via GPO preferences. As a backup, you can allow users to manually map as above.
​

