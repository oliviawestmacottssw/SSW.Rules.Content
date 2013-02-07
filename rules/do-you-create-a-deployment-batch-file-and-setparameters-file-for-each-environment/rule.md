---
type: rule
title: Do you Create a Deployment Batch file and SetParameters file for each Environment?
uri: do-you-create-a-deployment-batch-file-and-setparameters-file-for-each-environment
created: 2013-02-06T18:52:13.0000000Z
authors:
- id: 24
  title: Adam Stephensen

---

 This field should not be null (Remove me when you edit this field). ![](/TFS/Rules-to-Better-Continuous-Deployment/PublishingImages/setparameters.jpg)Figure: Good Example - The batch file specifies the target Server, the ProjectName name to deploy, and the configuration file to use. You can also optionally supply additional parameters. <br>      [Download a sample \_Deploy.bat file here as a .txt file](/TFS/Rules-to-Better-Continuous-Deployment/Documents/DeployBat.txt). ![](/TFS/Rules-to-Better-Continuous-Deployment/PublishingImages/batchfile.jpg)Figure: Good Example - The SetParameters file specifies MS Deploy parameterisation values.  Most important is the target “IIS Web Application Name” on the target server
See [Vishal’s blog](http&#58;//vishaljoshi.blogspot.com.au/2010/07/web-deploy-parameterization-in-action.html) for more details. 
