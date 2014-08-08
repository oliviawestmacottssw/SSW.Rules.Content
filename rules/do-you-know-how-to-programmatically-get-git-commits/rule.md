---
type: rule
title: Do you know how to programmatically get Git commits?
uri: do-you-know-how-to-programmatically-get-git-commits
created: 2014-08-07T23:07:23.0000000Z
authors:
- id: 38
  title: Drew Robson

---

 
​​​​​​​With [Visual Studio Online](http&#58;//www.visualstudio.com/) now supporting Git, ​​​​more developers are changing their source control repositories. What happens if an application you developed relies on the [TFS Client Object Model](http&#58;//msdn.microsoft.com/en-us/library/bb130146.aspx) to get information out of source control (e.g. changeset comments) and the developers start using Git?​
 
That's where the new [Visual Studio Online REST APIs](http&#58;//www.visualstudio.com/en-us/integrate/reference/reference-vso-overview-vsi.aspx) come in. You can get a list of commits from your VSO Git repository with only a HTTP request.​

​Using H​TTPS with basic authentication, make a GET request to a URL as below, substituting in your VSO details. A JSON object will be returned.

![8-08-2014-9-58-37-AM-compressor.png](/TFS/RulesToBetterVersionControlWithGit/PublishingImages/Pages/Do-you-know-how-to-programmatically-get-Git-commits/8-08-2014-9-58-37-AM-compressor.png)
**Figure: HTTPS GET commits from your VSO Git repository**

To quickly create classes from a JSON response, see the rule [Do you know how to easily get classes from a JSON response?](/SoftwareDevelopment/RulesToBetterWebAPI/Pages/Do-you-know-how-to-easily-get-classes-from-a-JSON-response.aspx)

​For implementation details, see this blog post.

(This is based on [Get started with the REST APIs](http&#58;//www.visualstudio.com/en-us/integrate/get-started/get-started-rest-basics-vsi.aspx) and [VSO Integration Reference](http&#58;//www.visualstudio.com/integrate/reference/reference-vso-git-overview-vsi))​

