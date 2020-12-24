---
type: rule
archivedreason: 
title: Do you Create a Deployment Batch file and SetParameters file for each Environment?
guid: 9a47c960-e98c-40d0-bb0f-2dbc164f476f
uri: do-you-create-a-deployment-batch-file-and-setparameters-file-for-each-environment
created: 2013-02-06T18:52:13.0000000Z
authors:
- id: 24
  title: Adam Stephensen
related: []
redirects: []

---

You should create a Deployment Batch file and SetParameters file for each Environment.

<!--endintro-->

[[goodExample]]
| ![The batch file specifies the target Server, the ProjectName name to deploy, and the configuration file to use. You can also optionally supply additional parameters..](setparameters.jpg)[Download a sample \_Deploy.bat file here as a .txt file](/Documents/DeployBat.txt)
[[goodExample]]
| ![The SetParameters file specifies MS Deploy parameterisation values.  Most important is the target “IIS Web Application Name” on the target serverfor more details.](batfile.jpg)[Vishal’s blog](http://vishaljoshi.blogspot.com.au/2010/07/web-deploy-parameterization-in-action.html)See
