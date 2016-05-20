---
type: rule
archivedreason: 
title: Do you have a migration plan
guid: 2f943ab1-a970-4c64-9f45-396f4d2d194a
uri: do-you-have-a-migration-plan
created: 2016-05-20T02:01:48.0000000Z
authors:
- title: Mark Liu
  url: https://ssw.com.au/people/mark-liu
- title: William Yin
  url: https://ssw.com.au/people/william-yin
related: []
redirects: []

---


<span style="line-height&#58;20.8px;">​​​At a high level, the plan is&#58;</span>
<br><excerpt class='endintro'></excerpt><br>
<p></p><p></p><ul><li><span style="line-height&#58;1.6;"><strong>Install </strong></span><span style="line-height&#58;1.6;"><strong>SharePoint&#160;​</strong></span><br></li></ul><ol><li><span style="line-height&#58;1.6;background-color&#58;initial;">I</span><span style="line-height&#58;1.6;background-color&#58;initial;">nstall with topology of your choice in SharePoint 2016 (or use <a href="https&#58;//autospinstaller.codeplex.com/">AutoSPInstaller</a>)</span><br></li><li><span style="line-height&#58;1.6;background-color&#58;initial;">Configure Application services</span><br></li></ol><p></p><p></p><blockquote style="margin&#58;0px 0px 0px 40px;border&#58;none;padding&#58;0px;"><ul><li>Run the wizard (or use script. the community script wasn't ready when Thiago and I was migrating intranet)​</li><li><span style="line-height&#58;1.5em;">Configure user profile and its permission configuration (see <a href="https&#58;//technet.microsoft.com/en-us/library/ee721052.aspx">msdn</a>​)​</span></li></ul></blockquote><div><div><ul><li><span style="line-height&#58;1.5em;"><strong>Test Migration</strong></span><br></li></ul></div><ol><li><span style="line-height&#58;1.6;"><a href="/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=50de290c-7bc6-4e9b-a784-e91367f2031d">Install required WSP packages in 2016</a></span><br></li><li><span style="line-height&#58;1.6;"><a href="/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=352a79b1-165c-411f-b3cd-0328c8a7b618">Test migrating&#160;content database from old to new</a>​</span></li><li>Fix all the missing customizations error in the above step, then do the <a href="https&#58;//technet.microsoft.com/en-us/library/ff607581%28v=office.16%29.aspx">content database migration</a></li><li><span style="line-height&#58;1.6;">(</span><span style="line-height&#58;1.6;">Optional) <a href="/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=65a88cf2-5b8e-4b13-a3e7-4e7c94ab7ea0">Migrate services database</a>&#160;(depends on which service applications do you use)</span><br></li></ol><ul><li><span style="line-height&#58;1.6;"><strong>Post migration setup</strong></span><br></li></ul><ol><li><span style="line-height&#58;1.6;">Configure search (TODO&#58; create a rule)</span><br></li><li><span style="line-height&#58;1.6;">Configure metadata (optional)</span><br></li></ol><ul><li><span style="line-height&#58;1.6;"><strong>Test test </strong></span><span style="line-height&#58;1.6;"><strong></strong></span><span style="line-height&#58;1.6;"><strong></strong></span><span style="line-height&#58;1.6;"><strong></strong></span><span style="line-height&#58;1.6;"><strong></strong></span><span style="line-height&#58;1.6;"><strong></strong></span><span style="line-height&#58;1.6;"><strong>tes</strong></span><span style="line-height&#58;1.6;"><strong>t</strong></span><br></li><li><span style="line-height&#58;1.6;"><strong>Go-live migration</strong></span><br></li></ul><ol><li><span style="line-height&#58;1.6;"><a href="/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=0ae3a717-ad22-4d2e-bd7c-a5f058393087">Put old SharePoint into read-only</a></span><br></li><li><span style="line-height&#58;1.6;"><a href="https&#58;//technet.microsoft.com/en-us/library/ff607581%28v=office.16%29.aspx">Refresh content &amp; service database from SP 2013 to 2016</a></span><br></li><li><span style="line-height&#58;1.6;">Update DNS</span><br></li><li><span style="line-height&#58;1.5em;">Decomission old SharePoint server and</span><span style="line-height&#58;1.5em;"> database (after 2 weeks when you're confident with the new environment)</span></li></ol><br><p><br></p></div>


