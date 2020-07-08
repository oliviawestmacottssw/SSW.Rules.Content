---
type: rule
archivedreason: 
title: Logon - Do you have a company-wide Word template?
guid: a58e2456-e070-4ddb-9ed8-996eab71ef90
uri: logon-do-you-have-a-company-wide-word-template
created: 2017-07-11T17:42:29.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
- title: Stanley Sidik
  url: https://ssw.com.au/people/stanley-sidik
- title: Kaique Biancatti
  url: https://ssw.com.au/people/kaique-biancatti
related:
- do-you-know-if-you-are-using-the-template
- do-you-use-great-email-signatures
redirects: []

---


A company-wide template will be implemented, so users have automatic footers to save time and give better branding.​​<br>
<dl class="badImage"><dt><img src="/PublishingImages/word-template-bad.jpg" alt="word-template-bad.jpg" /></dt><dd>Figure&#58; Bad Example - creating an email/document does not have the company templates</dd></dl><dl class="goodImage"><dt> <img src="/PublishingImages/word-template-good.jpg" alt="word-template-good.jpg" /></dt><dd>Figure&#58; Good Example - creating an email/document with the company templates​<br></dd></dl>
<br><excerpt class='endintro'></excerpt><br>
<p>How to have a company-wide Word template&#58;<br></p><ul><li>Modify your Normal.dotm file to have the headings and format that you want for Word document</li><li>Create standard employee email footer files e.g. JamesZhou.htm or JamesZhou.txt</li><li>Put the files on a network location - this is the place that will have the master copies&#160;<br></li><li>​Have a logon script which is set up through Group policy that will copy the file to the users' computer when they logon.<br>e.g. a PowerShell login script like <a href="https&#58;//github.com/SSWConsulting/SSWSysAdmins.LoginScript">https&#58;//github.com/SSWConsulting/SSWSysAdmins.LoginScript</a><br></li></ul><div><p class="ssw15-rteElement-CodeArea">ECHO Copy Office Templates To Workstation &gt;&gt; %LogonLogFile%<br>call %ScriptFolder%\SSWLogonScript\BatchScript\SafeCopyNewerFile.bat &quot;\\fileserver\DataSSW\DataSSWEmployees\Templates\Normal.dot&quot; &quot;%APPDATA%\Microsoft\Templates\Normal.dot&quot; %LogonLogFile%<br>call %ScriptFolder%\SSWLogonScript\BatchScript\SafeCopyNewerFile.bat &quot;\\fileserver\DataSSW\DataSSWEmployees\Templates\Normal.dotm&quot; &quot;%APPDATA%\Microsoft\Templates\Normal.dotm&quot; %LogonLogFile%<br>call %ScriptFolder%\SSWLogonScript\BatchScript\SafeCopyNewerFile.bat &quot;\\fileserver\DataSSW\DataSSWEmployees\Templates\ProposalNormalTemplate.dotx&quot; &quot;%APPDATA%\Microsoft\Templates\ProposalNormalTemplate.dotx&quot; %LogonLogFile%<br>call %ScriptFolder%\SSWLogonScript\BatchScript\SafeCopyNewerFile.bat &quot;\\fileserver\DataSSW\DataSSWEmployees\Templates\NormalEmail.dot&quot; &quot;%APPDATA%\Microsoft\Templates\NormalEmail.dot&quot; %LogonLogFile%<br>call %ScriptFolder%\SSWLogonScript\BatchScript\SafeCopyNewerFile.bat &quot;\\fileserver\DataSSW\DataSSWEmployees\Templates\Microsoft_Normal.dotx&quot; &quot;%APPDATA%\Microsoft\Templates\Microsoft_Normal.dotx&quot; %LogonLogFile%<br>call %ScriptFolder%\SSWLogonScript\BatchScript\SafeCopyNewerFile.bat &quot;\\fileserver\DataSSW\DataSSWEmployees\Templates\Blank.potx&quot; &quot;%APPDATA%\Microsoft\Templates\Blank.potx&quot; %LogonLogFile%<br>xcopy /Y &quot;\\fileserver\DataSSW\DataSSWEmployees\Templates\NormalEmail.dotm&quot; &quot;%APPDATA%\Microsoft\Templates\&quot; &gt;&gt; %LogonLogFile%<br>xcopy /Y &quot;\\fileserver\DataSSW\DataSSWEmployees\Templates\NormalEmail.dotx&quot; &quot;%APPDATA%\Microsoft\QuickStyles\&quot; &gt;&gt; %LogonLogFile%<br>ECHO Templates Copied <br></p><dd class="ssw15-rteElement-FigureNormal"></dd><dd class="ssw15-rteElement-FigureBad">Figure&#58; Bad Example - This is a snippet of an old login script</dd>​&#160;<br><p><b>Note&#58;</b> We don't want people using .RTF emails so we include this message in SSW.rtf. Be aware that we don't want to use RTF because of&#160;<a href="https&#58;//www.ssw.com.au/ssw/Standards/BetterSoftwareSuggestions/Outlook.aspx#RemoveRTF">Remove RTF as an option or explain when it is a good choice</a>.<br></p><p><b>Note&#58; </b>If you use a Mac computer, a login script will not work. In order to use a Word template, you must&#160;open the template&#160;on Word locally, hit &quot;Save as Template&quot;, and then upload that document to Teams.​<br></p><p class="ssw15-rteElement-YellowBorderBox"><b>Tip&#58;</b>&#160;You can automatically have your SSW Word doc template on&#160;sign-in via a script. See&#160;<a href="https&#58;//github.com/SSWConsulting/SSWSysAdmins.LoginScript">https&#58;//github.com/SSWConsulting/SSWSysAdmins.LoginScript</a><br></p></div>


