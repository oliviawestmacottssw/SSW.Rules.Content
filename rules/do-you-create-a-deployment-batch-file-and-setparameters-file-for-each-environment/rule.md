---
type: rule
archivedreason: 
title: Do you Create a Deployment Batch file and SetParameters file for each Environment?
guid: 9a47c960-e98c-40d0-bb0f-2dbc164f476f
uri: do-you-create-a-deployment-batch-file-and-setparameters-file-for-each-environment
created: 2013-02-06T18:52:13.0000000Z
authors:
- title: Adam Stephensen
  url: https://ssw.com.au/people/adam-stephensen
related: []
redirects: []

---


This field should not be null (Remove me when you edit this field).
<br><excerpt class='endintro'></excerpt><br>
<dl class="goodImage"><dt>
      <img src="/TFS/Rules-to-Better-Continuous-Deployment/PublishingImages/setparameters.jpg" alt="" />
   </dt><dd>Figure&#58; Good Example - The batch file specifies the target Server, the ProjectName name to deploy, and the configuration file to use. You can also optionally supply additional parameters. 
      <a href="/TFS/Rules-to-Better-Continuous-Deployment/Documents/DeployBat.txt">Download a sample _Deploy.bat file here as a .txt file</a>. </dd></dl><dl class="goodImage"><dt>
      <img src="/TFS/Rules-to-Better-Continuous-Deployment/PublishingImages/batchfile.jpg" alt="" /></dt><dd>Figure&#58; Good Example - The SetParameters file specifies MS Deploy parameterisation values.  Most important is the target “IIS Web Application Name” on the target server<br>See <a href="http&#58;//vishaljoshi.blogspot.com.au/2010/07/web-deploy-parameterization-in-action.html" target="_blank">Vishal’s blog</a> for more details. </dd></dl>


