---
type: rule
archivedreason: 
title: Do you publish your components to Source Safe?
guid: 4b133c80-e5f7-4649-9065-1ab750fccbee
uri: do-you-publish-your-components-to-source-safe
created: 2009-04-28T03:04:50.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
- title: Ryan Tee
  url: https://ssw.com.au/people/ryan-tee
related: []
redirects: []

---


This field should not be null (Remove me when you edit this field).
<br><excerpt class='endintro'></excerpt><br>

  <p>Corresponding with Microsoft's release of their application blocks, we've also started to build components and share them across projects.</p>
<p>Sharing a binary file with SourceSafe isn't a breeze to do, and here are the steps you need to take. It can be a bit daunting at first.</p>
<p>As the component developer, there are four steps&#58;</p>
<ol>
    <li>In Visual Studio.NET, Switch to release build<br>
    <img class="ms-rteCustom-ImageArea" alt="Build Release" src="/Standards/SoftwareDevelopment/RulesToBetterDotNETProjects/PublishingImages/build_release.jpg" /> <span class="ms-rteCustom-FigureGood">Figure&#58; Switch to release configuration</span> </li>
    <li>In your project properties, make sure the release configuration goes to the bin\Release? folder. While you are here, also make sure XML docs are generated. Use the same name as your dll but change the extension to .xml (eg. for SSW.Framework.Configuration.dll -&gt; add SSW.Framework.Configuration.xml)<br>
    <img class="ms-rteCustom-ImageArea" alt="Build Project Property" src="/Standards/SoftwareDevelopment/RulesToBetterDotNETProjects/PublishingImages/build_projectproperty_small.jpg" /> <span class="ms-rteCustom-FigureGood">Figure&#58; Project properties</span>
    <p>Note&#58; The following examples are considered being used for C#. Visual Basic, by default, does not have \bin\Release and \bin\Debug which which means that the debug and release builds will overwrite each other unless the default settings are changed to match C# (recommended). VB does not support XML comments either, please wait for the next release of Visual Studio (Whidbey). </p>
    <img class="ms-rteCustom-ImageArea" alt="Change to C#" src="/Standards/SoftwareDevelopment/RulesToBetterDotNETProjects/PublishingImages/changetocsharp.jpg" /> <span class="ms-rteCustom-FigureGood">Figure&#58; Force change to match C#</span> </li>
    <li>If this is the first time, include/check-in the release directory into your SourceSafe<br>
    <img class="ms-rteCustom-ImageArea" alt="Build Include" src="/Standards/SoftwareDevelopment/RulesToBetterDotNETProjects/PublishingImages/build_include.jpg" /> <span class="ms-rteCustom-FigureGood">Figure&#58; Include the bin\Release directory into source safe</span> </li>
    <li>Make sure everythings checked-in properly. When you build new versions, switch to Release?mode and checkout the release dlls, overwrite them, and when you check them back in they will be the new dll shared by other applications.</li>
    <li>
    <p>If the component is part of a set of components, located in a solution, with some dependency between them. You need to check out ALL the bin\Release folders for all projects in that solution and do a build. Then check in all of them. This will ensure dependencies between these components don't conflict with projects that reference this component set.</p>
    <p>In other words, a set of components such as SSW.Framework.WindowsUI.xxx, increment versions AS A WHOLE. One component in this set changes will cause the whole set to re-establish internal references with each other.</p>
    </li>
</ol>



