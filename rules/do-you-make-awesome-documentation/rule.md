---
type: rule
title: Do you make awesome documentation?
uri: do-you-make-awesome-documentation
created: 2012-03-16T08:01:26.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 23
  title: Damian Brady
- id: 3
  title: Eric Phan
- id: 4
  title: Ulysses Maclaren
- id: 24
  title: Adam Stephensen

---


There are 2 styles of documentation:
 
### Style #1: Old School:


| ​![IwS2](/SoftwareDevelopment/RulestobetterArchitectureandCodeReview/PublishingImages/iwS2.jpg) | ​This style of team does a lot of upfront documentation and planning, is very comfortable with Waterfall, and has rarely even heard of Agile :) |
| --- | --- |


- Heavy, long documents
- Sequence Diagrams​
- UML


This is a well established way to do documentation but the issue with it is that it gets out of date.
![enterprisearchitect1](/SoftwareDevelopment/RulestobetterArchitectureandCodeReview/PublishingImages/enterprisearchitect1.jpg)Figure: Documentation can take the form of Sequence Diagrams![enterprisearchitectusecases.png](/SoftwareDevelopment/RulestobetterArchitectureandCodeReview/PublishingImages/EnterpriseArchitectUseCases.jpg)Figure: ...or Use Case Diagrams 
Exception: Keep this limited to just enough documentation to cover a couple of sprints, and be committed to keeping it updated. The tool of choice if you're going down this road is Enterprise Architect (an excellent application built by Australians).

### Style #2: New School:


| ​![Mark Zuckerberg](/SoftwareDevelopment/RulestobetterArchitectureandCodeReview/PublishingImages/68843503-mark-zuckerberg.jpg) | ​This style of team are all under 30 and have never heard of FoxPro or Access |
| --- | --- |


- 6 small docs (a couple of pages max + in the order you would read them):
- Business.docx - Explaining the business purpose of the app
- Instructions\_Compile.docx - Contains instructions on <br>      [how to get the project to compile (aka the F5 experience)](/SoftwareDevelopment/RulesToBetterDotNETProjects/Pages/DoYouMakeInstructions.aspx)
- Instructions\_Deployment.docx - Describes the deployment process
- Technologies.docx - Explaining the technical overview e.g. Broad architecture decisions, 3rd party utilities, patterns followed etc.
- Definition\_Of\_Done.docx – Ensures that your team [maintains a high level of quality with a Definition of Done](/Management/RulesToSuccessfulProjects/Pages/Done-DefinitionOfDone.aspx)​
- Definition of Ready.docx – Ensure that your PBIs are well defined before adding them to a sprint by specifying a [Definition of Ready](/Management/RulesToBetterScrumUsingTFS/Pages/Definition-of-Ready.aspx)
- Unit Tests​
- Code and Work Items (Via the magic of Annotation)

![ProjectDocumentation.jpg](/SoftwareDevelopment/RulestobetterArchitectureandCodeReview/PublishingImages/ProjectDocumentation.jpg)Figure: 4 small docs explain most of what you need to know very briefly.![UnitTestExplorer.png](/SoftwareDevelopment/RulestobetterArchitectureandCodeReview/PublishingImages/UnitTestExplorer.png)Figure: Nice Unit Tests explain what the code is supposed to be doing.![vs11debug.png](/SoftwareDevelopment/RulestobetterArchitectureandCodeReview/PublishingImages/VS11Debug.png)Figure: Most young developers are happy with good old stepping through code with F11. The good thing is there are no diagrams that become out of date (which they always do after the first couple of sprints) giving you nasty Technical Debt.![tfspreviewbacklog.png](/SoftwareDevelopment/RulestobetterArchitectureandCodeReview/PublishingImages/TFSPreviewBacklog.jpg)Figure: Don't forget that you have the completed requirements which get done and archived and can now serve as free documentation e.g. User Stories (aka PBIs)![Annotation and Comment](/SoftwareDevelopment/RulestobetterArchitectureandCodeReview/PublishingImages/AnnotationAndComment.jpg)Figure: Annotations marry up the code with the PBIs, showing who, what, why and when for each piece of code

If you subscribe to this work item check in policy, then you understand that the PBI is now the documentation. If requirements change during the course of the PBI (based on a conversation with Product Owner of course) then the PBI should be updated.

When updating the acceptance criteria,           strike through the altered acceptance criteria and add the new ones. Get the PO to confirm your understanding.

E.g.
Enter search text, click ‘Google’, and see the results populate below.
[Updated]
 Enter search text and automatically see the results populate below.

This should be added to the           [definition of done](/Management/RulesToSuccessfulProjects/Pages/Done-DefinitionOfDone.aspx).


![Technical Debt](/SoftwareDevelopment/RulestobetterArchitectureandCodeReview/PublishingImages/Debt.jpg)
**What's "Technical Debt"?**

During a project, when you add functionality, you have a choice:

One way is quick but messy - it will make further changes harder in the future (i.e. quick and dirty).

The other way is cleaner – it will make changes easier to do in the future, but will take longer to put in place.

'Technical Debt' is a metaphor to help us think about this problem. In this metaphor (often mentioned during Scrum software projects), doing things the quick and dirty way gives us a 'technical debt', which will have to be fixed later. Like a financial debt, the technical debt incurs interest payments - in the form of the extra effort that we have to do in future development.

We can choose to continue paying the interest, or we can pay the debt up front by redoing the piece of work in the cleaner way.

The same principle is true with documentation. Using the 'old school' method will leave you with a build up of documentation that you will need to keep up-to-date as the project evolves.

Warning: if you want to follow Scrum and have zero technical debt, then you have to throw away all documentation at the end of each sprint. If you do want to keep it, make sure you add it to your           [definition of done](/Management/RulesToSuccessfulProjects/Pages/Done-DefinitionOfDone.aspx)to keep it updated.


