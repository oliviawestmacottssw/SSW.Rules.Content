---
type: rule
title: Do you enforce work item association with check-in?
uri: do-you-enforce-work-item-association-with-check-in
created: 2011-11-18T03:52:43.0000000Z
authors:
- id: 22
  title: David Klein
- id: 6
  title: Tristan Kurniawan
- id: 17
  title: Ryan Tee
- id: 5
  title: Justin King

---

 
One of the big advantage of using TFS is end to end traceability, however this requires the developer to do one extra step to link their code (changeset) with requirements (work items). Code is the body of software, while user requirement is the spirit. Work Item association feature helps us to link the spirit and body of software together. This is especially useful when you trying to identify the impact of a bug in term of user requirements.
 ![No work item associated](/PublishingImages/WorkItemAss-1.jpg)Figure: Bad Example: No work item is associated with changeset ![work item associated](/PublishingImages/WorkItemAss-2.jpg)Figure: Good Example: No work item is associated with changeset 
More Information 
In order to achieve this, developers need to choose the Work Item tab when check-in and "associate" code with a related work item.
![Work item association](/PublishingImages/WorkItemAss-3.jpg)Figure: Associate Work Item with Changeset 
As the project administrator, you can take one step further to enable "Work Item Check-in Policy" to enforce this rule in your team.
![Work Item Check-in Policy](/PublishingImages/WorkItemAss-4.jpg)Figure: Always enable the “Work Items check-in policy”
