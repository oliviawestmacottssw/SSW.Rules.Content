---
type: rule
title: Do you use subdomains instead of virtual directories?
uri: do-you-use-subdomains-instead-of-virtual-directories
created: 2013-10-14T07:53:27.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

Using subdomains over directories has 2 benefits:
 
1. it is easier to host different sections of your website on different platforms, and
2. in different geographic locations


​​​http://www.myservice.com/**ssw**/
http://www.myservice.com/**northwind**/

​​Figure: Bad Example - Virtual directories used to distinguish organizations



​​​​http://**ssw**.myservice.com/
http://**northwind**.myservice.com/

Figure: ​Good Example - S​ubdomains used to distinguish ​organizations
