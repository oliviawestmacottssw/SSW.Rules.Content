---
type: rule
archivedreason: We now use NuGet to manage dependencies
title: Do you write Integration Test for Dependencies - e.g. DLLs?
guid: 62615da5-6ce6-4f6d-b236-88cc2c918f93
uri: do-you-write-integration-test-for-dependencies-eg-dlls
created: 2020-03-11T21:59:13.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
related: []
redirects: []

---


Dependant code is code that relies on other factors like methods and classes inside a separate DLL. Because of the way the .NET works assemblies are loaded as required by the program (this is what we call the JIT compiler). Thus, when a DLL goes astray, you will only find out at run time when you run a form/function that uses that DLL. These run time errors can occur when you have not packaged DLLs in your release or if the versions are incompatible. Such errors cause the following exceptions&#58;<br>
<br><excerpt class='endintro'></excerpt><br>
<ul><li>An unhandled exception (&quot;System.IO.FileNotFoundException&quot;) occurred in SSW.NETToolkit.exe.</li><li>System.IO.FileLoadException The located assembly's manifest definition with name 'SSW.SQLDeploy.Check' does not match the assembly reference.</li></ul><p>These errors can be fixed by writing a integration test to check all referenced assemblies in a project.</p><p>Sample code&#58;<b></b></p><p class="ssw15-rteElement-CodeArea">[Test]<br>public void ReferencedAssembliesTest()<br>&#123;<br> // Get the executing assembly<br> Assembly asm = Assembly.GetExecutingAssembly();<br> // Get the assemblies that are referenced<br> AssemblyName[] refAsms = asm.GetReferencedAssemblies();<br> // Loop through and try to load each assembly<br> foreach( AssemblyName refAsmName in refAsms)<br> &#123;<br> try<br> &#123;<br> Assembly.Load(refAsmName);<br>  &#125;<br> catch(FileNotFoundException)<br> &#123;<br> // Missing assembly<br> Assert.Fail(refAsmName.FullName + &quot; failed to load&quot;);<br> &#125;<br> &#125;<br>&#125;</p><dd class="ssw15-rteElement-FigureNormal">​​​Figure&#58; This code is a unit test for checking that all referenced assemblies are able to load.</dd><p><br></p>


