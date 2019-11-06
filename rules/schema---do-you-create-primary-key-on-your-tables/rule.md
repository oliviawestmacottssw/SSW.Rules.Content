

---
authors:
  - id: 1
    title: Adam Cogan
---




<span class='intro'> ​​When you specify a PRIMARY KEY constraint for a table, SQL Server enforces data uniqueness by creating a unique index for the primary key columns. This index also permits fast access to data when the primary key is used in queries.<p class="ssw15-rteElement-P">Although, strictly speaking, the primary key is not essential&#160;- we recommend all tables have a primary key (except tables that have a high volume of continuous transactions).&#160;<br></p><dl class="ssw15-rteElement-ImageArea"><img src="/PublishingImages/SqlTableWithoutPrimaryKey.PNG" alt="" style="margin&#58;5px;" /></dl><dd class="ssw15-rteElement-FigureBad">Figure&#58; Bad Example - Table missing primarykey<br></dd><dl class="ssw15-rteElement-ImageArea">​<img src="/PublishingImages/SqlTableWithPrimaryKey.PNG" alt="" style="margin&#58;5px;" /></dl><dd class="ssw15-rteElement-FigureGood">Figure&#58; Good Example - Table with primary key<br></dd><dl class="ssw15-rteElement-ImageArea"><br></dl><p class="ssw15-rteElement-P"><strong>Legacy&#58;</strong>&#160;<br></p><p class="ssw15-rteElement-P">Especially, when you have a client like Access, it would help you to avoid the problems.​​</p> </span>



