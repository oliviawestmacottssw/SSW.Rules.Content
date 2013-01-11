---
type: rule
archivedreason: 
title: C#/VB.NET Configuration - Do you know not to use debug compilation in production applications?
guid: b50ed5b1-e954-4b6c-bc92-f159228150dc
uri: c-vbnet-configuration-do-you-know-not-to-use-debug-compilation-in-production-applications
created: 2013-01-11T18:25:53.0000000Z
authors: []
related: []
redirects: []

---


<p>Debug compilation considerably increases memory footprint since debug symbols are required to be loaded. </p>
<p>Additionally it will hit the performance because that will include the optional debug and trace statements in the output IL code.</p>

<br><excerpt class='endintro'></excerpt><br>
<p>In debug mode the compiler emits debug symbols for all variables and compiles the code as is. In release mode some optimizations are included&#58;</p>
<ul>
<li>unused variables do not get compiled at all</li>
<li>some loop variables are taken out of the loop by the compiler if they are proven to be invariants</li>
<li>code written under #debug directive is not included etc.</li>
</ul>
<p>The rest is up to the JIT.</p>
<p>As per&#58; <a target="_blank" href="http&#58;//stackoverflow.com/questions/2446027/c-sharp-debug-vs-release-performance"></a>C# debug vs release performance.</p>

<dl>
<dt><img src="/SoftwareDevelopment/RulesToBetterDotNETProjects/PublishingImages/debug-bad.jpg" alt="" /></dt>
<dd>Figure&#58; Bad Example</dd>
</dl>

<dl>
<dt><img src="/SoftwareDevelopment/RulesToBetterDotNETProjects/PublishingImages/debug-good.jpg" alt="" /></dt>
<dd>Figure&#58; Good Example</dd>
</dl>



