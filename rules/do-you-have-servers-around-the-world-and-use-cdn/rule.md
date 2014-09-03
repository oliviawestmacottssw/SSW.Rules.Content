---
type: rule
title: Do you have servers around the world and use CDN?
uri: do-you-have-servers-around-the-world-and-use-cdn
created: 2014-09-03T19:17:30.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

 Having a very popular website is great. The only problem is where to host it. If you host it in your local country then it is very fast for your local market but what about the market on the other side of the world? 
The solution is to have 2 or more servers and direct users to the server that is                     the closest to them. This is possible with the help of Bind DNS server and a list                     of IP addresses and the country of origin.

The beauty of this solution is that it is not application specific. Anything like                     VoIP or game servers can be directed to their local server.
                     Follow the directions found in this article http://peen.net/2006/03/08/geo-dns to                     setup your Bind config file. The only problem is that the PHP script supplied in                     that article does not work correctly. It cannot convert the number based IP to the                     real IP and subnet. Because of this I had to create my own little app to make the                     file for Bind to use. You can find it and get the [source code](/Documents/IpToCountryConverter.zip).

You can download a free list of IP to country’s from [http://software77.net/cgi-bin/ip-country/geo-ip.pl](/ssw/Redirect/Software77.htm)

**How it works:
**Once you have made your acl files you can use views in the bind configuration                     to specify which zone file to use for each group of IP’s. Each zone file would                     have the relevant IP information for that target segment of the world.

Imagine you have 3 zone files: one for europe, one for the america’s and one                     for the rest of the world. You simple edit named.conf.local to include the acls                     for europe and the america’s. E.g.:
               include "/etc/bind/named.conf.options";<br>
<br>               include "/etc/bind/acl-europe\_east.inc";<br>
<br>               include "/etc/bind/acl-europe\_sout.inc";<br>
<br>               include "/etc/bind/acl-europe\_west.inc";<br>
<br>               include "/etc/bind/acl-europe\_nort.inc";<br>
<br>               include "/etc/bind/acl-america\_cari.inc";<br>
<br>               include "/etc/bind/acl-america\_cent.inc";<br>
<br>               include "/etc/bind/acl-america\_nort.inc";<br>
<br>               include "/etc/bind/acl-america\_sout.inc";<br>

<br>               Next you create separate views. One for europe, one for the america’s <br>               and one for everyone else.<br>
<br>               view "europe" {<br>
<br>                match-clients {<br>
<br>                 europe\_east;<br>
<br>                 europe\_nort;<br>
<br>                 europe\_sout;<br>
<br>                 europe\_west<br>
<br>                };<br>
<br>                zone "peen.net" {<br>
<br>                 type master;<br>
<br>                 file "/etc/bind/europe/db.peen.net";<br>
<br>                };<br>
<br>               };<br>

<br>               view "americas" {<br>
<br>                match-clients {<br>
<br>                 america\_cari;<br>
<br>                 america\_nort;<br>
<br>                 america\_sout;<br>
<br>                 america\_cent<br>
<br>                };<br>
<br>                zone "peen.net" {<br>
<br>                 type master;<br>
<br>                 file "/etc/bind/americas/db.peen.net";<br>
<br>                };<br>
<br>               };<br>

<br>               view "others" {<br>
<br>                match-clients { any; };<br>
<br>                zone "peen.net" {<br>
<br>                 type master;<br>
<br>                 file "/etc/bind/others/db.peen.net";<br>
<br>                };<br>
<br>               };​  
