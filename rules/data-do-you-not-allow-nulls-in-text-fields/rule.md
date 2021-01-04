---
type: rule
archivedreason: 
title: Data - Do you not allow Nulls in text fields?
guid: c1b019ad-1c24-4960-9d0a-bf4e0924d8e5
uri: data-do-you-not-allow-nulls-in-text-fields
created: 2019-11-23T00:18:45.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
related: []
redirects: []

---


​​NULLs complicate your life. To avoid having to constantly differentiate between empty strings and NULLs, you should avoid storing NULLS if you can.<p class="ssw15-rteElement-P">Why? Well, what is wrong with this?​​​<br></p>
<br><excerpt class='endintro'></excerpt><br>
<p class="ssw15-rteElement-CodeArea">​SELECT ContactName FROM Customer WHERE ContactName <> ''<br></p><dd class="ssw15-rteElement-FigureNormal">Figure: Selecting on empty string​<br></dd><p>Nothing if your data is perfect, but if you allow Nulls in your database, then statements like this will give you unexpected results. To get it working you would have to add the following to the last line:</p><p class="ssw15-rteElement-CodeArea">WHERE ContactName <> '' OR ContactName Is Null </p><dd class="ssw15-rteElement-FigureNormal">Figure: Allowing null strings makes queries more complex<br><br></dd><p>What about only allowing empty strings? Well, we choose to block Nulls because it is a lot easier to check off a check box in SQL Server Management Studio than it is to put a constraint on every field that disallows empty string ('').​<br></p><dl class="image"><dt><img src="SqlTableWithNullValue.PNG" alt="" style="margin:5px;" /><br></dt><dd>Figure: Don't allow Nulls​</dd></dl><p>However, you should always be aware that Nulls and empty strings are totally different, so if you absolutely have to have them, they should be used consistently. In the ANSI SQL-92 standard, an empty string ('') is never equated to Null, because empty string can be significant in certain applications. </p><p><strong>Not allowing Nulls will give you the following benefits: </strong><br></p><ul><li>​​​​​Don't have to enforce every text field with a CHECK constraint such as ([ContactName]<>'').</li><li>Make your query simpler, avoid extra checking in stored procedures. So you don't have to check for NULLs and empty strings in your WHERE clause.<br></li><li>SQL Server performs better when nulls are not being used.<br></li><li>Don't have to deal with the pain in the middle tier to explicitly check DBNull.Value, you can always use contactRow.ContactName == String.Empty. Database Nulls in the .NET framework are represented as DBNull.Value and it cannot implicitly typecast to ANY other type, so if you are allowing NULLs in ContactName field, the above comparing will raise an exception.</li><li>Avoid other nasty issues, a lot of controls in the .NET framework have real problems binding to DBNull.Value. So you don't have write custom controls to handle this small thing.<br></li></ul><p></p><p>For example, you have Address1 and Address2 in your database, a Null value in Address2 means you don't know what the Address2 is, but an empty string means you know there is no data for Address2. You have to use a checkbox on the UI to explicitly distinguish Null value and empty string:​<br></p><dl class="image"><dt>
         <img src="NullValueOnUI.jpg" alt="NullValueOnUI.jpg" />
         <br>
      </dt><dd>​Figure: A check box is required if you want to allow user to use Null value on the UI</dd></dl><p>Some people are not going to like this rule, but this is how it works in Oracle and Access:<br></p><ul><li>In Oracle, empty strings are turned into Nulls (which is basically what this rule is doing). Empty strings per se are not supported in Oracle (This is not ANSI compliant).</li><li>And talking of legacy systems :-) be aware that using Access as a data editor is a "No-No". Access turns empty strings into a Null.</li></ul><p></p><p>Finally, always listen to the client, Nulls have meaning over an empty string - there are exceptions where you might use them - but they are rare.</p><p>So follow this rule, block Nulls where possible, update your NULLs with proper information as soon as possible, and keep data consistent and queries simple.<br></p>


