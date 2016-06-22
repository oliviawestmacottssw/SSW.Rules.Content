---
type: rule
archivedreason: 
title: Do you know the quickest way to get your Windows 10 SOE up and running?
guid: 434aba3a-381a-474c-b8d3-357d10fc55bf
uri: do-you-know-the-quickest-way-to-get-your-windows-10-soe-up-and-running
created: 2016-06-20T04:57:19.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
- title: Stanley Sidik
  url: https://ssw.com.au/people/stanley-sidik
- title: Kaique Biancatti
  url: https://ssw.com.au/people/kaique-biancatti
related: []
redirects: []

---


​<p>Your developers should be using Windows 10 for a <a href="http&#58;//au.pcmag.com/windows-10-preview-release-date-news-features/35511/feature/10-reasons-to-upgrade-to-windows-10"><span lang="EN-US" style="text-decoration&#58;underline;">number of reasons</span></a>, the primary one being it is faster than Windows 8. </p><p>The next step is to get the Standard Operating Environment (SOE) installed. You have a few choices&#58;</p><ul><li>Manually - it can take over a day to install your favourite 20 or so apps</li><li>Windows Image - there is overhead of maintaining the .WIM file as software changes</li><li>Use a package manager (eg. chocolatey) - RECOMMENDED</li></ul>
<br><excerpt class='endintro'></excerpt><br>
<h3 class="ssw15-rteElement-H3">​Use a package manager (chocolatey)&#160;</h3>
<br>Assuming that Windows 10 in already installed, then get your SOE installed fast by following these steps&#58; 
<ol style="list-style-type&#58;decimal;"><li>Logon and configure Windows 10</li><li>Install Windows Updates​​​</li><li>Join&#160;laptop to&#160;the Domain (or run a Logon-Script.bat to get printers, Word templates etc. Contact SysAdmin to join laptop to domain)<br></li><li>Run&#160;a 
      <a href="https&#58;//sugarlearning.com/companies/SSW/items/8159/it-infrastructure-configure-your-laptop">Chocolatey script</a> to get most of the software</li><li>Install all rest of the standard 
      <a href="https&#58;//sugarlearning.com/companies/SSW/items/8159/it-infrastructure-configure-your-laptop">Software</a> that does not&#160;support Chocolatey</li><li>In case you lose your laptop, it is a good idea to stick a business card to the bottom </li><li>For branding reasons, stick your company sticker to the laptop</li></ol><p></p><dl class="image"><dt>
      <img src="/SiteAssets/do-you-know-the-quickest-way-to-get-your-windows-10-soe-up-and-running/LoginScript.jpg" alt="LoginScript.jpg" style="margin&#58;5px;width&#58;808px;" />​<span style="color&#58;#555555;font-size&#58;0.9rem;font-weight&#58;bold;line-height&#58;16px;">&quot;Figure&#58; SSWLoginScript.bat&quot;</span> </dt></dl><p></p><dl class="image"><dt>
      <img src="/SiteAssets/do-you-know-the-quickest-way-to-get-your-windows-10-soe-up-and-running/ChocolateyScript.jpg" alt="ChocolateyScript.jpg" style="margin&#58;5px;width&#58;808px;height&#58;428px;" />​<span style="color&#58;#555555;font-size&#58;0.9rem;font-weight&#58;bold;line-height&#58;16px;">&quot;Figure&#58; SSWPackages.ps1 which runs Chocolatey command to install SOE&#160;software&quot;</span> </dt></dl><dl class="image"><dt> 
      <img src="/SiteAssets/do-you-know-the-quickest-way-to-get-your-windows-10-soe-up-and-running/NonChocolateySoftware.jpg" alt="NonChocolateySoftware.jpg" style="margin&#58;5px;width&#58;808px;" />
   </dt><dt>
      <span style="color&#58;#555555;font-size&#58;14.4px;font-weight&#58;bold;line-height&#58;16px;">&quot;Figure&#58; SOE Software that are not supported by&#160;Chocolatey&quot;</span>​ </dt></dl><dl class="image"><dt>
<img src="/SiteAssets/do-you-know-the-quickest-way-to-get-your-windows-10-soe-up-and-running/SSWLaptopBranding.jpg" alt="SSWLaptopBranding.jpg" style="margin&#58;5px;" />
</dt><dt>
 <span style="color&#58;#555555;font-size&#58;14.4px;font-weight&#58;bold;line-height&#58;16px;">&quot;Figure&#58; SOE Software that are not supported by&#160;Chocolatey&quot;</span>​</dt></dl>


