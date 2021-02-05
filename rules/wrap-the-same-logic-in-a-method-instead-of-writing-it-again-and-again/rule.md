---
type: rule
archivedreason: 
title: Do you wrap the same logic in a method instead of writing it again and again whenever it's used?
guid: 68299342-ec35-4f73-a340-4fdf7eb2144d
uri: wrap-the-same-logic-in-a-method-instead-of-writing-it-again-and-again
created: 2018-04-26T23:35:54.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
related: []
redirects:
- do-you-wrap-the-same-logic-in-a-method-instead-of-writing-it-again-and-again-whenever-its-used

---


<p class="ssw15-rteElement-P">Is your code DRY? ​​Any logic that is used more than once, should be encapsulated in a method, and the method called wherever it is needed.<br><br></p><p class="ssw15-rteElement-P">This will reduce redundancy, decrease maintenance effort, improve efficiency and reusability, and make the code more clear to read.​​​​<br></p>
<br><excerpt class='endintro'></excerpt><br>
<p class="ssw15-rteElement-CodeArea">public class WarningEmail<br>&#123;<br>//...<br>public void SendWarningEmail(string pFrom, string pTo, string pCC, string pUser, string pPwd, string pDomain)<br>&#123;<br>//...<br>MailMessage sMessage = new MailMessage();<br>sMessage.From = new MailAddress(pFrom);<br>sMessage.To.Add(pTo);<br>sMessage.CC.Add(pCC);<br>sMessage.Subject = &quot;This is a Warning&quot;;<br>sMessage.Body = GetWarning();<br>SmtpClient sSmtpClient = new SmtpClient();<br>sSmtpClient.Credentials = new NetworkCredential(pUser, pPwd, pDomain);<br>sSmtpClient.Send(sMessage);<br>//...<br>&#125;<br>&#125;<br>public class ErrorEmail<br>&#123;<br>public void SendErrorEmail(string pFrom, string pTo, string pCC, string pUser, string pPwd, string pDomain)<br>&#123;<br>//...<br>MailMessage sMessage = new MailMessage();<br>sMessage.From = new MailAddress(pFrom);<br>sMessage.To.Add(pTo);<br>sMessage.CC.Add(pCC);<br>sMessage.Subject = &quot;This is a Error&quot;;<br>sMessage.Body = GetError();<br>SmtpClient sSmtpClient = new SmtpClient();<br>sSmtpClient.Credentials = new NetworkCredential(pUser, pPwd, pDomain);<br>sSmtpClient.Send(sMessage);<br>//...<br>&#125;<br>&#125;<br></p><dd class="ssw15-rteElement-FigureBad">Bad Example&#58; Write the same logic repeatedly <br></dd><p>
   <br>
</p><p class="ssw15-rteElement-CodeArea">public class WarningEmail<br>&#123;<br>//...<br>public void SendWarningEmail(string pFrom, string pTo, string pCC, string pUser, string pPwd, string pDomain)<br>&#123;<br>//...<br>EmailHelper.SendEmail(pFrom, pTo, pCC, &quot;This is a Warning&quot;, GetWarning(), pUser, pPwd, pDomain);<br>//...<br>&#125;<br>&#125;<br>public class ErrorEmail<br>&#123;<br>public void SendErrorEmail(string pFrom, string pTo, string pCC, string pUser, string pPwd, string pDomain)<br>&#123;<br>//...<br>EmailHelper.SendEmail(pFrom, pTo, pCC, &quot;This is an Error&quot;, GetError(), pUser, pPwd, pDomain);<br>//...<br>&#125;<br>&#125;<br>public class EmailHelper<br>&#123; <br>public static void SendEmail(string pFrom, string pTo, string pCC, string pSubject, string pBody, string pUser, string pPwd, string pDomain)<br>&#123;<br>MailMessage sMessage = new MailMessage();<br>sMessage.From = new MailAddress(pFrom);<br>sMessage.To.Add(pTo);<br>sMessage.CC.Add(pCC);<br>sMessage.Subject = pSubject;<br>sMessage.Body = pBody;<br>SmtpClient sSmtpClient = new SmtpClient();<br>sSmtpClient.Credentials = new NetworkCredential(pUser, pPwd, pDomain);<br>sSmtpClient.Send(sMessage);<br>&#125; <br>&#125;<br></p><dd class="ssw15-rteElement-FigureGood">Good Example&#58; Put the same logic in a method and make it reusable​ <br><br><br></dd>


