---
type: rule
title: Do you know how to manage NuGet packages with Git?
uri: do-you-know-how-to-manage-nuget-packages-with-git
created: 2014-10-23T04:30:48.0000000Z
authors:
- id: 38
  title: Drew Robson
- id: 44
  title: Duncan Hunter

---

 ​​​​Do you know the best way to manage NuGet packages with Git? You can get into all sorts of trouble by including your packages in source control. 
The following are a few issues that are related to having your NuGet packages in source control:

1. Over time the packages will grow to be too many and cloning the repository will be slow.
2. You could get duplicate NuGet packages in your packages folder as new versions are updated.
3. NuGet shows packages to update that have already been updated. This can happen if you have duplicate NuGet packages but they are different versions.
4. It becomes harder to "clean" your solution of any unused package folders, as you need to ensure you don't delete any package folders still in use.


​In order to track your repositories.config and make use of NuGet Package Restore to ​restore missing packages when a build begins, complete the following steps:

1. ​Read the NuGet offical documentation on http://docs.nuget.org/docs/reference/package-restore
2. Enable NuGet Package Restore for your solution by right clicking on your solution name in the Solution Explorer& and selecting Enable NuGet Package Manage Restore from the drop down menu.<br>   ![nuget package restore2.png](/TFS/RulesToBetterVersionControlWithGit/PublishingImages/Pages/Do-you-know-how-to-manage-NuGet-packages-with-Git/Enable%20package%20restore%202014-10-23_17-43-13.png)
3. Go to Team Explorer in Visual Studio and select Settings.<br>   ![Team explorer home](/TFS/RulesToBetterVersionControlWithGit/PublishingImages/Pages/Do-you-know-how-to-manage-NuGet-packages-with-Git/Team%20explorer%20home%202014-10-23_14-39-49.png)​
4. Choose Git Settings under Git. <br>   ![Team-Explorer compressor](/TFS/RulesToBetterVersionControlWithGit/PublishingImages/Pages/Do-you-know-how-to-manage-NuGet-packages-with-Git/Team-Explorer-2014-10-23_14-40-48-compressor.png)
5. Choose /.gitIgnore<br>   ![Git Settings](/TFS/RulesToBetterVersionControlWithGit/PublishingImages/Pages/Do-you-know-how-to-manage-NuGet-packages-with-Git/Git%20Settings%202014-10-23_14-41-22.png)
6. In the gitIgnore file find and uncomment the repositories.config line to include it in source control.<br>   ![git-ignore-image-compressor.png](/TFS/RulesToBetterVersionControlWithGit/PublishingImages/Pages/Do-you-know-how-to-manage-NuGet-packages-with-Git/git-ignore-image-2014-10-23_14-27-55-compressor.png)
7. rebuild your solution and you can now safely delete your packages folder and NuGet Package Restore will restore any missing NuGet packages on each new build. You will not need to add your package folder to your repository after these steps.​​​​​​

 ​  
