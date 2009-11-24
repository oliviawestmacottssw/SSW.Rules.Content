---
type: rule
archivedreason: 
title: Do you have a rollback plan?
guid: f13a6fd0-9137-4981-a613-3408b36c0229
uri: do-you-have-a-rollback-plan
created: 2009-11-02T22:38:45.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
- title: Eric Phan
  url: https://ssw.com.au/people/eric-phan
related: []
redirects: []

---



  <p style="margin-right&#58;0px;" dir="ltr">Always plan for a catastrophic disaster, in the event of errors when testing&#58;</p>
<ol>
    <li>Take the&#160;TFS2010 server offline </li>
    <li>Bring the TFS2008 server online </li>
    <li>Change the DNS entries for tfs.northwind.com from the IP for the TFS2010 server to the IP for the TFS2008 server
    <ol>
        <li>Internal DNS Server </li>
        <li>External DNS Server</li>
    </ol>
    </li>
</ol>
<p>TODO&#58; Add figure of DNS pointers.</p>

<br><excerpt class='endintro'></excerpt><br>



