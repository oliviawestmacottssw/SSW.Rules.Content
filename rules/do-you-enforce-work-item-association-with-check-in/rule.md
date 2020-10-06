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
 
[[badExample]]
| ![No work item is associated with changeset](WorkItemAss-1.jpg)
[[goodExample]]
| ![No work item is associated with changeset](WorkItemAss-2.jpg)
More Information 
In order to achieve this, developers need to choose the Work Item tab when check-in and "associate" code with a related work item.

![Associate Work Item with Changeset](WorkItemAss-3.jpg)
As the project administrator, you can take one step further to enable "Work Item Check-in Policy" to enforce this rule in your team.

![Always enable the “Work Items check-in policy”](WorkItemAss-4.jpg)
