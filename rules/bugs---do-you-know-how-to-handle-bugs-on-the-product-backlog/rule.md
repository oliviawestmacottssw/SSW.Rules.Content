---
type: rule
title: Bugs - Do you know how to handle Bugs on the Product Backlog?
uri: bugs---do-you-know-how-to-handle-bugs-on-the-product-backlog
created: 2010-05-06T04:38:50.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 14
  title: Martin Hinshelwood
- id: 3
  title: Eric Phan

---


Story Points cannot be allocated against bugs in MSF Agile 5.0 so to include them in a Sprint we need to group them.

Bugs that are introduced and found because of the current work in the Sprint are included in the Sprint and estimated immediately so the burndown remains accurate.

See [Do you know when to create bugs?](/Management/RulesToBetterScrumUsingTFS/Pages/CreateBugs.aspx) for detailed information on identifying when something is a bug, and when to just fix it.

1. ## Using MSF Agile 5.0
    Bugs found that are independent of the work on the current Sprint are placed on the Product Backlog as a work item “Bug”. The product Owner then ranks the Bugs with priority amongst the User Stories. Bugs cannot have Story Points allocated to them so User Stories need to be created with Bugs as Child Work Items. This is only done when the PO has prioritized the Bug and the Bug is likely to make the next Sprint. At the Planning Meeting, the PO elects which Bugs are to be included and new User Stories are created to group them appropriately with due regard to Severity and Stack Rank. Once the User Stories have been created, The Team estimates the Story Points for each one; the Product confirms User Stack Rank and the Sprint Backlog is planned as normal.
    This process:

    - Works around the problem of Bugs not having Story Points
    - Allows Bugs of the same rank to be sensibly grouped together
    - Prevents arbitrary groupings of Bugs which cannot be properly ranked
    - Follows the estimate just-in-time philosophy of Scrum
    - Prevents small Bugs taking up a whole Story Point
2. ## Using Visual Studio Scrum 1.0
    In the Visual Studio Scrum template bugs are just another PBI and you can assign a business priority and an effort estimate in Story Points. Bugs that make the cut for the next sprint can be broken down into tasks and estimated as required.
    As bugs from previous sprints are just PBI’s, the PO agrees to a list of bugs that will be fixed in the current Sprint.
    The team just fixes any **newly** bugs they introduced in the current sprint.
    If the team finds bugs due to functionality accepted in a previous sprint they log it as a PBI and will complete the fix in a future sprint, unless it is a critical bug, in which case they raise it as an impediment to the current sprint to the PO.


Examples:

- **Small bug** – Text on a label is spelled incorrectly
- **Big bug** - There is an error thrown when transitioning from page 1 to page 2 when you hold down the Ctrl key


