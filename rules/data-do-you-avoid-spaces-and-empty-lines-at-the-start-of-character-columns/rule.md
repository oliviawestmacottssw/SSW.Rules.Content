---
type: rule
archivedreason: 
title: Data - Do you avoid spaces and empty lines at the start of character columns?
guid: 848bd3dc-36eb-408f-a216-ce06bb730c54
uri: data-do-you-avoid-spaces-and-empty-lines-at-the-start-of-character-columns
created: 2019-11-25T19:01:24.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
- title: Christian Morford-Waite
  url: https://ssw.com.au/people/christian-morford-waite
related: []
redirects: []

---


<p class="ssw15-rteElement-P">​​​Text in character columns (char, varchar, text, nchar, varchar, text) can start with spaces or empty lines which is usually data entry error.​<br></p><p class="ssw15-rteElement-P">The best way to avoid this issue is to handle whitespace in the middle-tier before it reaches the database.<br>However, if you are using stored procedures you can also remove leading&#160;spaces using <a href="https&#58;//docs.microsoft.com/en-us/sql/t-sql/functions/ltrim-transact-sql?view=sql-server-ver15">LTRIM (Transact-SQL)​</a>.<br></p>
<br><excerpt class='endintro'></excerpt><br>
<p>​If you are trying to remove carriage returns you can use the following SQL&#58;</p><p class="ssw15-rteElement-CodeArea">​DECLARE @TextString VARCHAR(500)<br>SET @TextString = '''<br>a<br>b<br>'''<br>SELECT @TextString as 'With carriage returns'<br>SELECT REPLACE(REPLACE(@TextString,char(10),''),char(13),'') as 'Without carriage returns'​<br><br></p><dd class="ssw15-rteElement-FigureNormal">​​Figure&#58; SQL script to remove carriage returns from string.<span style="background-color&#58;initial;">​</span><span style="background-color&#58;initial;">​</span></dd><dl class="ssw15-rteElement-ImageArea"><img src="/PublishingImages/SqlRemovingCarriageReturns.jpg" alt="" style="margin&#58;5px;" /></dl><dd class="ssw15-rteElement-FigureNormal">Figure&#58; Example of carriage returns removed with the above SQL snippet.​<br></dd>


