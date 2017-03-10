---
type: rule
archivedreason: 
title: Do you use the Code Health Extensions in VS Code?
guid: ba1170f1-3d1a-4af1-b35e-b0c82b5b6ac2
uri: do-you-use-the-code-health-extensions-in-vs-code
created: 2017-03-09T22:12:04.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
- title: Danijel Malik
  url: https://ssw.com.au/people/danijel-malik
related: []
redirects: []

---


For lightweight web projects such as Angular, often VS Code is more appropriate than Visual Studio. So&#160;make sure your code quality remains consistent with CssLint and TSLint.<br>
<br><excerpt class='endintro'></excerpt><br>
<h3 class="ssw15-rteElement-H3">Related Steps to Code Health&#58;<br></h3><ul><li><a href="/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=b30bb5f2-6ac1-4f56-8975-dad84b0ba489">Do
you<span style="font-family&#58;calibri;font-size&#58;11pt;"> know the Code Health (Quality Gates) to add?</span></a><br></li><li><a href="/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=9e155c90-0502-447a-a1a3-fb2b1580982a">Do you use the Code Health Extensions in Visual Studio?</a><br></li><li><a href="/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=3c2f0b76-038b-47c2-a754-f897f9d502ef">Do you run the Code Health checks in your VisualStudio.com Continuous Integration Bu<span style="font-family&#58;calibri;font-size&#58;11pt;">ild?​​</span></a><br></li></ul><h3 class="ssw15-rteElement-H3">Which E​xtensi​​​ons​ to Use​ in VS Code<br></h3><p>​For web projects, we advocate the use of CSSLint for css files and TSLint for typescript files. (<a href="/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=d82703e0-6244-4fb6-9017-bac4e4b2361d">Why you should be using TypeScript instead of JavaScript​​</a>)<br>Linters for these can be easily added to VS Code via extensions.<br>Simply select the &quot;Extensions&quot; tab, search for &quot;CSSLint&quot; and &quot;TSLint&quot; and click &quot;Install&quot; on each respectively.​</p><dl class="ssw15-rteElement-ImageArea">​​<img src="/SiteAssets/do-you-use-the-code-health-extensions-in-vs-code/VSCode-Extensions.png" alt="VSCode-Extensions.png" style="margin&#58;5px;width&#58;650px;" /></dl><dd class="ssw15-rteElement-FigureNormal">Figure&#58; Addition of CssLi​nt and TSLint to VS Code Project</dd><p>If you prefer not to use the Extensions (which are currently a bit out of date). You can install them using npm as normal.​​<br>CssLint (<a href="https&#58;//www.npmjs.com/package/csslint%E2%80%8B">Csslint npm guide</a>)<br>TSLint (<a href="https&#58;//www.npmjs.com/package/tslint%20%E2%80%8B">TSlint npm guide​</a>)<br><br></p>


