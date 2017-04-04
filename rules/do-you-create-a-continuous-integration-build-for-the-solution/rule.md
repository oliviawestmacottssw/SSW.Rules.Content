---
type: rule
title: Do you create a Continuous Integration Build for the Solution?
uri: do-you-create-a-continuous-integration-build-for-the-solution
created: 2013-02-06T18:49:06.0000000Z
authors:
- id: 24
  title: Adam Stephensen

---

 
​​(Before you configure continuous deployment) You need to ensure that the code that you have on the server compiles. A successful CI build without deployment lets you know the solution will compile.
 ![](/PublishingImages/ci-build-1.jpg)Figure: The Build definition name should include the project name. The reason for this is that builds for all solutions are placed in the same folder, and including the build name makes the Build Drop folder organised![](/PublishingImages/ci-build-2.jpg)Figure: On the Trigger tab choose Continuous Integration. This ensures that each check-in results in a build![](/PublishingImages/ci-build-3.jpg)Figure: On the Workspace tab you need to include all source control folders that are required for the build![](/PublishingImages/ci-build-4.jpg)Figure: Enter the path to your Drop Folder (where you drop your builds)![](/PublishingImages/ci-build-5.jpg)Figure: Choose the Default Build template and enter the DeployOnBuild argument to the MSBuild Arguments parameter of the build template![](/PublishingImages/ci-build-6.jpg)Figure: Queue a build, to ensure our CI build is working correctly![](/PublishingImages/ci-build-7.jpg)Figure: Before we setup continuous deployment it is important to get a successful basic CI build
