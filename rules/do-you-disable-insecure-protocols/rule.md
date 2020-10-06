---
type: rule
title: Do you disable insecure protocols?
uri: do-you-disable-insecure-protocols
created: 2017-11-02T22:51:47.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 71
  title: Steven Andrews

---

For better server security (especially regarding public facing servers), certain security protocols and ciphers should be disabled.

 
Using a tool called "IIS Crypto 2.0" by     [Nartac](https://www.nartac.com/Products/IISCrypto), these protocols can be easily disabled instead of having to manually edit the Registry Keys.

1. Download IIS Crypto 2.0 (https://www.nartac.com/Products/IISCrypto/Download)
2. Run this on the server you wish to lock down
3. Select the best practices button <br>      
[[goodExample]]
| ![TLS should be enabled and SSL should be disabled](IIS Crypto 2.0.png)
4. Ensure that TLS 1.0 is also disabled and hit apply <br>
5. The server will need to be rebooted before the settings take effect
