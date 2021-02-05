---
type: rule
archivedreason: 
title: ​DBAs - Do you configure all your SQL Server Services to use a Domain Account rather than a local service account?
guid: 8592bce1-390d-4d01-b459-630c3efea01b
uri: configure-all-your-sql-server-services-to-use-a-domain-account
created: 2019-11-18T19:52:14.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
related: []
redirects:
- dbas-do-you-configure-all-your-sql-server-services-to-use-a-domain-account-rather-than-a-local-service-account

---


<p>Depending on which components you decide to install on your SQL Server, you may need to configure the following services​:<br><br></p><ul><li>SQL Server<br></li><li>SQL Server Agent<br></li><li>SQL Server Reporting Services</li><li>SQL Server Integration Services<br></li><li>SQL Server Fulltext search</li><li>SQL Server Analysis Services<br></li></ul><p>In the service properties window for these services, ensure that the Service Startup Account is run as "This Account" and not as "Built-in Account". Otherwise, you won't get all the functionality by default such as the ability to use Replication, Linked Servers or connect to other machines.<br></p><p>For security, you should not have this domain account​ in the Administrators group.​<br><br></p>
<br><excerpt class='endintro'></excerpt><br>
<dl class="badImage"><dt>
      <img src="SQLDatabases_RunAsAccount_Bad.png" alt="SQLDatabases_RunAsAccount_Bad.png" />
   </dt><dd>Figure: Bad example - This service is using a built-in local service account​</dd></dl><dl class="goodImage"><dt>
         <img src="SQLDatabases_RunAsAccount.png" alt="SQLDatabases_RunAsAccount.png" />
         <br>
      </dt><dd>​Figure: Good example - Run as Account should use a domain account rather than a built-in account​</dd>
</dl>


