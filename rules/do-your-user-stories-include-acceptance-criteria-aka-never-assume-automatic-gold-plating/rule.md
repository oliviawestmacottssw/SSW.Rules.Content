---
type: rule
title: Do Your User Stories Include Acceptance Criteria? (aka Never assume automatic Gold Plating)
uri: do-your-user-stories-include-acceptance-criteria-aka-never-assume-automatic-gold-plating
created: 2011-05-30T08:13:44.0000000Z
authors:
- id: 24
  title: Adam Stephensen

---


Most teams are getting the hang of User Stories that have sub tasks. Unfortunately the same can’t be said about acceptance criteria. 
 It is so important because real user stories tell a team when the task is done.

Also Product Owners should not get heartburn because ‘obvious’ functionality was not included. All requirements should be specified in the Acceptance Criteria.
 For example, Product Owners should not assume things like:

- they will get a message that says ‘no records found’ or
- the grid will support features such as pagination or sorting


They must be specified in the Acceptance Criteria if required.

There are 2 parts to getting this right. The Acceptance Criteria, then the Acceptance Tests:

**Acceptance Criteria **(from the Product Owner) define the exact requirements that must be met for the story to be completed. They answer the question, "How will I know when I’m done with the story?"
![A User Story with Acceptance Criteria](/Management/RulesToBetterScrumUsingTFS/PublishingImages/acceptance-criteria.jpg) Figure: A User Story with Acceptance Criteria (MSF Agile Template)

When I enter ‘Adam’ in the search box and click ‘Search’ I will see all entries starting with ‘Adam’ in the grid
Figure: Bad Example of Acceptance Criteria - Incomplete
Positive Test -When I enter ‘Adam’ in the Search box and click ‘Search’ I will see all entries starting with Adam in the Grid
 Negative Test - When I enter ‘zzz’ in the Search box and click ‘Search’ I will see \*no\* entries in the Grid
Figure: OK Example of Acceptance Criteria
Positive Test -When I enter ‘Adam’ in the Search box and click ‘Search’ I will see all entries starting with Adam in the Grid
 Negative Test - When I enter ‘zzz’ in the Search box and click ‘Search’ I will see \*no\* entries in the Grid
 Gold Plating - If no results are retuned show a message box ‘No results found’
 Gold Plating – Validation: If no search text is entered, the ‘Search’ button should be disabled
 Gold Plating – Right clicking on a column header should provide ‘Sort’ functionality
 Gold Plating – if a large set of results is returned, display pagination with page numbers and ‘Prev’, ‘Next’ links
 Figure: Good Example of Acceptance Criteria – Including Gold Plating



**Acceptance Tests** (built by the developers) verify that the Acceptance Criteria are met.
 The goal is for teams to move beyond manual testing and implement automated testing 
 eg. CodedUI tests, Telerik Tests etc
  Test cases answer the question, "How do I test and what are the test steps?"
![Test Cases in a User Story](/Management/RulesToBetterScrumUsingTFS/PublishingImages/acceptance-criteria-test-cases.jpg)Figure: Test Cases in a User Story  (MSF For Agile Template)

Positive Test -When I enter ‘Adam’ in the Search box and click ‘Search’ I will see all entries starting with Adam in the Grid
 Negative Test - When I enter ‘zzz’ in the Search box and click ‘Search’ I will see \*no\* entries in the Grid
 Gold Plating - If no results are retuned show a message box ‘No results found’
 Gold Plating – Validation: If no search text is entered, the ‘Search’ button should be disabled
 Gold Plating – Validation: If the button is disable and search text is entered, the ‘Search’ button becomes enabled
 Gold Plating – Right clicking on a column header and using the ‘Sort’ functionality, sorts the data by that column
 Gold Plating – if a large set of results is returned, clicking the pagination page numbers shows the correct data
 Gold Plating – if a large set of results is returned and we are on page &gt; 1, clicking the ‘Prev’ button goes to the previous page
 Gold Plating – if a large set of results is returned and we are on page 1, ‘Prev’ button does not error
 Gold Plating – if a large set of results is returned and we are on page &lt; MaxPage, clicking the ‘Next’ button goes to the next page
 Gold Plating – if a large set of results is returned and we are on page = MaxPage, clicking the ‘Next’ button does not error
 Figure: Good example - Acceptance Tests![Test Cases](/Management/RulesToBetterScrumUsingTFS/PublishingImages/test-cases.jpg)Figure: The tester sees the Test Cases in Test Manager![Test Steps](/Management/RulesToBetterScrumUsingTFS/PublishingImages/test-steps.jpg)Figure: The tester follows each instruction (aka the Test Steps), and gives it a tick or cross
## Related Resources

[http://www.scrumalliance.org/articles/169-new-to-user-stories](http&#58;//www.scrumalliance.org/articles/169-new-to-user-stories)

