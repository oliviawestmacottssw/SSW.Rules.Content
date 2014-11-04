---
type: rule
archivedreason: 
title: Do you know how to manage NuGet packages with Git?
guid: eb767a37-edb7-44cd-981a-5207fafa41e5
uri: do-you-know-how-to-manage-nuget-packages-with-git
created: 2014-10-23T04:30:48.0000000Z
authors:
- title: Drew Robson
  url: https://ssw.com.au/people/drew-robson
- title: Duncan Hunter
  url: https://ssw.com.au/people/duncan-hunter
related: []
redirects: []

---


​​​​​​Do you know the best way to manage NuGet packages with Git? You can get into all sorts of trouble by including your packages in source control.
<br><excerpt class='endintro'></excerpt><br>
<div><p><br></p><p>The following are a few issues that are related to having your NuGet packages in source control&#58;</p><ol><li>Over time the packages will grow to be too many and cloning the repository will be slow.</li><li>You could get duplicate NuGet packages in your packages folder as new versions are updated.</li><li>NuGet shows packages to update that have already been updated. This can happen if you have duplicate NuGet packages but they are different versions.</li><li>It becomes harder to &quot;clean&quot; your solution of any unused package folders, as you need to ensure you don't delete any package folders still in use.</li></ol><br></div><div><br></div><div>Automatic Package Restore in Visual Studio&#160;</div><div>Beginning with NuGet 2.7, the NuGet Visual Studio extension integrates into Visual Studio's build events and restores missing packages when a build begins. This feature is enabled by default and packages.config will be automatically included in souce control.</div><div></div><div><br><p><span style="line-height&#58;20px;">Here's how it works&#58;</span><br></p></div><div><ol><li><span style="line-height&#58;20px;">On project or solution build, Visual Studio raises an event that a build is beginning within the solution.</span><br></li><li><span style="line-height&#58;20px;">NuGet responds to this event and checks for&#160;packages.config&#160;files included in the solution.</span><br></li><li><span style="line-height&#58;20px;">For each&#160;packages.config&#160;file found, its packages are enumerated and checked for existence in the solution's&#160;packages&#160;folder.</span><br></li><li><span style="line-height&#58;20px;">Any missing packages are downloaded from the user's configured (and enabled) package sources, respecting the order of the package sources.</span><br></li><li><span style="line-height&#58;20px;">As packages are downloaded, they are unzipped into the solution's&#160;packages&#160;folder.</span><span style="line-height&#58;20px;">​</span><br></li></ol><p><br></p><p>You can read more here&#160;<a href="http&#58;//blogs.msdn.com/b/dotnet/archive/2013/08/22/improved-package-restore.aspx?PageIndex=3#comments" style="font-family&#58;calibri, sans-serif;font-size&#58;11pt;line-height&#58;1.6;">http&#58;//blogs.msdn.com/b/dotnet/archive/2013/08/22/improved-package-restore.aspx?PageIndex=3#comments</a>.</p><p>​<br></p><p>If you are using a&#160;version of&#160;NuGet prior to version 2.7 then the below steps outline how to avoid including packges in source control&#160;&#58;</p><ol><li>​Read the <a href="http&#58;//docs.nuget.org/docs/reference/package-restore">offical&#160;NuGet documentation​</a></li><li>Enable NuGet Package Restore for your solution by right clicking on your solution name in the Solution Explorer&#160;and select&#160;Enable NuGet Package Manage Restore from the drop down menu.
   <dl class="image"><dt><img src="/TFS/RulesToBetterVersionControlWithGit/PublishingImages/Pages/Do-you-know-how-to-manage-NuGet-packages-with-Git/Enable%20package%20restore%202014-10-23_17-43-13.png" alt="nuget package restore2.png" style="width&#58;489px;" /></dt></dl></li><li>Go to Team Explorer in Visual Studio and select Settings.
   <dl class="image"><dt><img src="/TFS/RulesToBetterVersionControlWithGit/PublishingImages/Pages/Do-you-know-how-to-manage-NuGet-packages-with-Git/Team%20explorer%20home%202014-10-23_14-39-49.png" alt="Team explorer home" />​</dt></dl></li><li>Choose Git Settings under Git. 
   <dl class="image"><dt><img src="/TFS/RulesToBetterVersionControlWithGit/PublishingImages/Pages/Do-you-know-how-to-manage-NuGet-packages-with-Git/Team-Explorer-2014-10-23_14-40-48-compressor.png" alt="Team-Explorer compressor" /></dt></dl></li><li>Choose /.gitIgnore
   <dl class="image"><dt><img src="/TFS/RulesToBetterVersionControlWithGit/PublishingImages/Pages/Do-you-know-how-to-manage-NuGet-packages-with-Git/Git%20Settings%202014-10-23_14-41-22.png" alt="Git Settings" /></dt></dl></li><li>In the gitIgnore file find and uncomment the repositories.config line to include it in source control.
   <dl class="image"><dt><img src="/TFS/RulesToBetterVersionControlWithGit/PublishingImages/Pages/Do-you-know-how-to-manage-NuGet-packages-with-Git/git-ignore-image-2014-10-23_14-27-55-compressor.png" alt="git-ignore-image-compressor.png" style="width&#58;550px;" /></dt></dl></li><li>Rebuild your solution and you can now safely delete your packages folder and NuGet Package Restore will restore any missing NuGet packages on each new&#160;build. You will not need to add your package folder to your repository after these steps.​​​​​​</li></ol>
​</div>


