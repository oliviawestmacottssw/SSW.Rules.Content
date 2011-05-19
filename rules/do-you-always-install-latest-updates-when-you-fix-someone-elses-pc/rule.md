---
type: rule
title: Do you always install latest updates when you fix someone else's PC?
uri: do-you-always-install-latest-updates-when-you-fix-someone-elses-pc
created: 2009-03-09T06:56:48.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 47
  title: Stanley Sidik

---

 When you fix someone else's PC (locally or remotely), one of the best practices is always make sure it has the latest updates. <br> 
To achieve this, we run [Microsoft Updates](http&#58;//www.ssw.com.au/ssw/Redirect/MicrosoftUpdate.htm) (**not** to confuse with Windows Updates) and install all latest updates for all the known Microsoft products.

Note: "Windows Update" only updates the operating system, where "Microsoft Update" updates other products as well, such as Microsoft Office, SQL Server, etc.
![Microsoft Update](/PublishingImages/MicrosoftUpdateGood.gif) Figure: Microsoft Update (Good - all updates are installed)
And then we run [SSW Diagnostics](http&#58;//www.ssw.com.au/ssw/Diagnostics) to check the latest version of other applications (mostly non-Microsoft) are installed.

Warning: Of course if you are fixing a bug on someone’s PC, you should only update one piece of software at a time, so you know if an update fixes the problem. After that (if the company allows it), update all software to the latest version. If they get a new problem, then rollback.
  ![SSW Diagnostics](/PublishingImages/DiagnosticsGood_small.jpg) Figure: SSW Diagnostics (Good - all updates are installed)
