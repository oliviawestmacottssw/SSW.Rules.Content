---
type: rule
archivedreason: 
title: Do you know how to programmatically get Git commits?
guid: 4a4daa31-0812-4975-bc5b-52066e3b1dd6
uri: do-you-know-how-to-programmatically-get-git-commits
created: 2014-08-07T23:07:23.0000000Z
authors:
- title: Drew Robson
  url: https://ssw.com.au/people/drew-robson
related: []
redirects: []

---


<p>​​​​​​​With <a href="http&#58;//www.visualstudio.com/">Visual Studio Online</a> now supporting Git, ​​​​more developers are changing their source control repositories. What happens if an application you developed relies on the <a href="http&#58;//msdn.microsoft.com/en-us/library/bb130146.aspx">TFS Client Object Model</a> to get information out of source control (e.g. changeset comments) and the developers start using Git?​</p>
<br><excerpt class='endintro'></excerpt><br>
<p>That's where the new <a href="http&#58;//www.visualstudio.com/en-us/integrate/reference/reference-vso-overview-vsi.aspx">Visual Studio Online REST APIs</a> come in. You can get a list of commits from your VSO Git repository with only a HTTP request.​</p><p>​Using&#160;H​TTPS with basic authentication, make a GET request to a URL as below, substituting in your VSO details. A JSON object will be returned.</p><p><img src="/TFS/RulesToBetterVersionControlWithGit/PublishingImages/Pages/Do-you-know-how-to-programmatically-get-Git-commits/8-08-2014-9-58-37-AM-compressor.png" alt="8-08-2014-9-58-37-AM-compressor.png" style="margin&#58;5px;width&#58;650px;" /><br><strong>Figure&#58; HTTPS GET commits from your VSO Git repository</strong></p><p><span style="line-height&#58;20.799999237060547px;"><br>To quickly create classes from a JSON response, see the rule&#160;<a href="/SoftwareDevelopment/RulesToBetterWebAPI/Pages/Do-you-know-how-to-easily-get-classes-from-a-JSON-response.aspx">Do you know how to easily get classes from a JSON response?</a></span></p><p><span style="line-height&#58;20.799999237060547px;">​For implementation details, see this blog post.</span></p><p><span style="line-height&#58;20.799999237060547px;">(This is based on&#160;</span><a href="http&#58;//www.visualstudio.com/en-us/integrate/get-started/get-started-rest-basics-vsi.aspx" style="line-height&#58;20.799999237060547px;">Get started with the REST APIs</a><span style="line-height&#58;20.799999237060547px;">&#160;and&#160;</span><a href="http&#58;//www.visualstudio.com/integrate/reference/reference-vso-git-overview-vsi" style="line-height&#58;20.799999237060547px;">VSO Integration Reference</a><span style="line-height&#58;20.799999237060547px;">)​</span><br></p>


