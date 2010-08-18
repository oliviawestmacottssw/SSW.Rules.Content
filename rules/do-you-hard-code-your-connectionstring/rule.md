---
type: rule
archivedreason: 
title: Do you hard code your ConnectionString?
guid: 601cfc39-e263-423b-b2ab-f0d3fa50fdda
uri: do-you-hard-code-your-connectionstring
created: 2009-04-29T05:36:44.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
- title: Ryan Tee
  url: https://ssw.com.au/people/ryan-tee
related: []
redirects: []

---


We don't like hard coded string inside our programme. We are using model-driven development, in which we create or reuse code, and perform changes in configuration file rather the in-code changing. <a href="/Standards/SoftwareDevelopment/RulesToBetterDotNETProjects/Pages/ConfigurationManagementAppBlock.aspx" id="More information on implementing our configuration">More information on implementing our configuration</a>. 

<br><excerpt class='endintro'></excerpt><br>

  <pre class="brush&#58;c-sharp">connection.ConnectionString = &quot;
Provider=SQLOLEDB;
Data Source=server_name_or_address; Initial Catalog=database_name;
User ID=username; Password=password; &quot;;

   connection.Open();
</pre>
<span class="ms-rteCustom-FigureBad">Bad code - use the lengthy connection string.</span>
<pre class="brush&#58;c-sharp">connection.ConnectionString = ConfigurationManager.Items[&quot;ConnectionString&quot;];

 connection.Open();
</pre>
<span class="ms-rteCustom-FigureGood">Figure&#58; Good Code - Use ConfigurationManager to handle the connection string.</span>
<table id="table30" class="clsSSWProductTable" cellspacing="2" summary="Code Auditor" cellpadding="2">
    <tbody>
        <tr>
            <td>We have a program called <a href="http&#58;//www.ssw.com.au/ssw/CodeAuditor/Default.aspx">SSW Code Auditor</a> to check for this rule. </td>
        </tr>
    </tbody>
</table>



