---
type: rule
title: Do you know the 3 steps to a PBI?
uri: do-you-know-the-3-steps-to-a-pbi
created: 2013-08-30T06:33:21.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 3
  title: Eric Phan

---

 ​​​The lifecycle of a PBI can be broken down into 3 steps: 
### 1. Ready

1. Take the next PBI that was created by the Product Owner
2. Is the PBI ready?
Check your PBI against your Definition of Ready. “Ready” PBIs must have Acceptance Criteria. A good Definition of Ready also encourages a test first mentality in requirements e.g. Use Spec Flow (Given, When, Then) and/or create Test Cases and Test Steps first.
3. Break down your PBI into tasks.
4. Don't forget to make a task for testing! (So that it is visible in the task board).

 ![Testing task.png](/PublishingImages/Testing%20task.png) Figure: Testing Task added to PBI
### 2. Code

1. Create a branch for your PBI
2. On the Web Task Board, move your Task into “In Progress”
3. Code, code, commit… Code, code, commit (Red Green Refactor)
4. As you complete tasks, move them to “Done”
5. Repeat 2-4
6. If you want feedback early, record a video. E.g. Snagit


### 3. Done

Is the PBI “Done”? Check your Definition of Done, and then the Tester:

1. Open a pull request
2. Do an "over the shoulder" check of the code
3. Use [Microsoft's "Exploratory Tester" Chrome extension](/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=14be0d02-79ad-4286-8b78-4f28b0ed4eea) to test the app
4. Make changes based on feedback (and then get more feedback)
5. Merge changes to master, this automatically deploys (to either Test, Staging or Prod based on process maturity)
6. Send a "done" email

​Congrats. Your PBI is now ready to be demonstrated during your Sprint Review! (Note: This is also the same process you follow for a Bug work item)  ![3StepsToAPBI.jpg](/PublishingImages/3StepsToAPBI.jpg) Good Figure: This image includes all the important steps in a PBI lifecycle. Print this "[SSW 3 Steps to a PBI pdf](/Documents/3StepsToAPBI.pdf)" and put it on your 'War Room' wall.
