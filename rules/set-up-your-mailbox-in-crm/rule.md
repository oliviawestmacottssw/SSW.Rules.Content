---
type: rule
archivedreason: 
title: Do you set up your mailbox in CRM?
guid: 7ff2d0a5-bdd4-4874-9c85-98d3f8b4cd68
uri: set-up-your-mailbox-in-crm
created: 2020-09-17T21:24:52.0000000Z
authors:
- title: Kaique Biancatti
  url: https://ssw.com.au/people/kaique-biancatti
related: []
redirects:
- do-you-set-up-your-mailbox-in-crm

---


<p class="ssw15-rteElement-P">If you want to track appointments and emails in Microsoft Dynamics 365 (CRM), you first need to set up your mailbox in the system.<br></p><p class="ssw15-rteElement-P">​Do the following:​​​​<br></p>
<br><excerpt class='endintro'></excerpt><br>
<ol><li>Browse to your Dynamics 365 Online URL | Advanced Settings | Settings | Email Configuration | Mailboxes | Browse for your mailbox:
   <dl class="image"><dt><img src="crm-open-meilbox-settings.png" alt="crm-open-meilbox-settings.png" style="width:750px;" /></dt><dd>Figure: You should see your mailbox. Click the link on Name and it will open up your mailbox settings<br></dd></dl></li><li>Make sure the following options are set (they might differ a bit depending on your CRM configuration): 
      <ul><li><b>Allow to Use Credentials for Email Processing:</b> checked</li><li><b>User Name:</b> &lt;YourUserName@yourcompany.com&gt;</li><li><b>Password:</b> &lt;YourPassword&gt;</li><li><b>cServer Profile:</b> Exchange Online Hybrid</li><li><b>Incoming Mail:</b> Server-Side Synchronization or Email Router</li><li><b>Outgoing Mail:</b> Server-Side Synchronization or Email Router</li><li><b>Appointments, Contacts, and Tasks:</b> Server-Side Synchronization</li></ul></li><li>Click <b>Test & Enable Mailbox</b><br>If successful, you will receive an email, if not, contact your nearest SysAdmin<br><br></li><li>Click Save & Close!</li></ol><dl class="image"><dt>
      <img src="setup-mailbox-crm.png" alt="setup-mailbox-crm.png" style="width:750px;" />
   </dt><dd>Figure: Setting up your mailbox in CRM<br></dd></dl><p>If you need more guidance on setting it up, you can find more on Microsoft documentation: <a href="https://docs.microsoft.com/en-us/dynamics365/customerengagement/on-premises/admin/set-incoming-outgoing-email-synchronization">Set incoming and outgoing email synchronization</a>.</p><p>After this is done, you should install the Dynamics 365 App for Outlook: <a href=/install-the-2-add-ins>https://rules.ssw.com.au/dynamics-crm-install-the-dynamics-365-app-for-outlook</a><br></p>


