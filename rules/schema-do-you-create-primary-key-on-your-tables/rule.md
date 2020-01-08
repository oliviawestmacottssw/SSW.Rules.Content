---
type: rule
archivedreason: 
title: Schema - Do you create primary key on your tables?
guid: c4682407-cea8-469a-abe4-8ddb795a986a
uri: schema-do-you-create-primary-key-on-your-tables
created: 2019-11-05T23:57:23.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
related: []
redirects: []

---


​When you specify a PRIMARY KEY constraint for a table, SQL Server enforces data uniqueness by creating a unique index for the primary key columns. This index also permits fast access to data when the primary key is used in queries.<p class="ssw15-rteElement-P">Although, strictly speaking, the primary key is not essential&#160;- we recommend all tables have a primary key (except tables that have a high volume of continuous transactions).&#160;<br></p><p class="ssw15-rteElement-P"><strong>Legacy&#58;</strong>&#160;<br></p><p class="ssw15-rteElement-P">Especially, when you have a client like Access, it would help you to avoid the problems.​​</p>
<br><excerpt class='endintro'></excerpt><br>



