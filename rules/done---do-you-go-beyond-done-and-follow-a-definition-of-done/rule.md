---
type: rule
title: Done - Do you go beyond 'Done' and follow a 'Definition of Done'?
uri: done---do-you-go-beyond-done-and-follow-a-definition-of-done
created: 2010-02-10T00:09:02.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 12
  title: Peter Gfader
- id: 13
  title: Paul Neumeyer
- id: 23
  title: Damian Brady

---

 ​Having a clear Definition of Done for your team is critical to your success and quality management in Scrum.

Every team is different, but all need to agree on which items are in their "Definition of Done".  
# There are 3 levels of "Done" in communication

## Level 1

- Sending a ["Done" email](/dones-do-you-reply-done-and-delete-the-original-email)​


## Level 2

- Sending a "Done" email
- screenshots
- code


## Level 3

- Sending a "Done" email
- video
- code (showing a full scenario e.g. a user story)​


#### Example of a level 3 "done"


Subject: RE: Manad - Coded UI Tests #2

&gt; Create a new CodedUI test on your feedback form – search only to test the Telerik

Done
![Coded UI Test passes in Visual Studio](/PublishingImages/level-3-done.jpg)Figure – Coded UI Test passes in Visual Studio
Jing Video of the test running:        [http://screencast.com/t/ps17fqsV](http&#58;//screencast.com/t/ps17fqsV)

Figure: Good example - The "done" shows a full scenario
# There are 8 levels of "Done" in software quality

Start with these examples showing typical "Definitions of Done" from beginner teams to more mature teams:

## Team - Level 1

- The code compiles
- All tasks are updated and closed
- No high priority defects/bugs are on that user story


## Team - Level 2

- *All of the above, plus*
- All unit tests passed
- Greater than 1% code coverage (not earth shattering, but you need to start somewhere)


## Team - Level 3

- *All of the above, plus*
- Successful build on the Build Server
- Check in Policy - Changeset Comments Policy (all checkins must have a comment)
- Check in Policy - Work Items (all checkins must be associated with a work item)
- Code reviewed by one other team member (e.g. Checked by Bill)
- Sending a Done email with screenshots

![Check in policy](/PublishingImages/CheckinPolicy.jpg)Figure: Good example - Add check in policies to enforce your Definition of Done
## Team - Level 4

- *All of the above, plus*
- All acceptance criteria have been met
- All acceptance criteria have an associated test passing (aka. Automated functional testing with Web Tests (Selenium), Coded UI Tests, or Telerik Tests)
- Sending a Done email (with video recording using Jing)

![Acceptance Tests in MTM](/PublishingImages/AcceptanceTestsInMTM.jpg)Figure: Good example - Acceptance Tests in MTM
## Team - Level 5

- *All of the above, plus*
- Deployed to UAT (ideally using Continuous Deployment)
- Complex code is documented (removing technical debt)
- Product Owner acceptance


## Team - Level 6

- *All of the above, plus*
- Multiple environments automatically tested using Lab Management

![Lab management](/PublishingImages/LabManagement.jpg)Figure: Good example - A tester Lab Management to create VMs for testing the application, then defines a test plan for that application with Test Case Management
## Team - Level 7

- *All of the above, plus*
- Automated Load Testing
- Continuous Deployment

![Acceptance Tests in MTM](/PublishingImages/LoadTesting.jpg)Figure: Good example - Load testing involves multiple test agents running Web Performance Tests and pounding the application (simulating the behaviour of many simultaneous users)**Team - Level 8 (Gold)**
- *All of the above, plus*
- Deployed to Production


Congratulations! You are frequently deploying to production. This is called “Continuous Delivery” and allows you to gather quick feedback from your end users.
 

*You might have everything deployed to production, but it might not yet be visible to the end user. This can be achieved by having “*[*Feature toggles*](http&#58;//martinfowler.com/bliki/FeatureToggle.html) *” in place. The actual release of the functionality is a decision that the Product Owner and business takes.*


**More Information:​**

- [Do your user stories include acceptance criteria?](/do-your-user-stories-include-acceptance-criteria-%28aka-never-assume-automatic-gold-plating%29)
- [Do you enforce comments with check-ins?](http&#58;//www.ssw.com.au/ssw/Standards/Rules/RulesToBetterSourceControlwithTFS.aspx#EnforceComments "Do you enforce comments with check-ins?")
- [Do you enforce work item association with check-in?](http&#58;//www.ssw.com.au/ssw/Standards/Rules/RulesToBetterSourceControlwithTFS.aspx#EnforceWorkItemAss "Do you enforce work item association with check-in?")
- [Do you follow a Test Driven Process?](http&#58;//www.ssw.com.au/ssw/Standards/Rules/RulesToBetterVersionControlwithTFS%28AKASourceControl%29.aspx#TestDrivenProcess "Do you follow a Test Driven Process?")
- 
- [Do you have a "Definition of Ready"?](/do-you-have-a-＂definition-of-ready＂)


