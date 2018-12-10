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


​There are 2 styles of documentation:
 
### Level 1 - Old School



| ​![IwS2](/PublishingImages/iwS2.jpg) | This team style does a lot of upfront documentation and planning, is very comfortable with Waterfall, and has rarely even heard of Agile :) |
| --- | --- |


- Heavy, long documents
- Sequence Diagrams
- UML


This is a well-established way to do documentation but the issue with it is that it gets out of date.
![enterprisearchitect1](/PublishingImages/enterprisearchitect1.jpg)Figure: Documentation can take the form of Sequence Diagrams![enterprisearchitectusecases.png](/PublishingImages/EnterpriseArchitectUseCases.jpg)Figure: ...or Use Case Diagrams 
**Exception:** Keep this limited to just enough documentation to cover a couple of sprints, and be committed to keeping it updated. The tool of choice if you're going down this road is Enterprise Architect (an excellent application built by Australians).

### Level 2 - Lots of documentation (and the 6 important documents)



| ​![Mark Zuckerberg](/PublishingImages/68843503-mark-zuckerberg.jpg) | This team style are all under 30 and have never heard of FoxPro or Access<br> |
| --- | --- |


6 small docs (a couple of pages max + in the order you would read them):

- Documentation\Business.docx - Explaining the business purpose of the app
- Documentation\Instructions-Compile.docx - Contains instructions on <br>      [how to get the project to compile (aka the F5 experience)](/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=d6d34c31-ac6a-49a4-876a-f9d30e1ab78a)
- Documentation\Instructions-Deployment.docx - Describes the deployment process
- Documentation\Patterns-and-Technologies.docx - Explaining the technical overview e.g. Broad architecture decisions, 3rd party utilities, patterns followed etc. (ie. SSW Data Onion)
- Documentation\Definition-of-Done.docx – Ensures that your team <br>      [maintains a high level of quality with a Definition of Done](/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=6449ae79-ba88-447e-aa48-36173029a2af)​
- Documentation\Definition-of-Ready.docx – Ensure that your PBIs are well defined before adding them to a sprint by specifying a <br>      [Definition of Ready](/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=637c230e-b1e3-4f2e-b2e0-c1a5431c1758)
- Unit Tests
- Code and Work Items (Via the magic of Annotation)

![ProjectDocumentation.jpg](/PublishingImages/ProjectDocumentation.jpg)Figure: 6 small docs explain most of what you need to know very briefly

### Level 3: Go Markdown

![vsts-wiki.jpg](/PublishingImages/vsts-wiki.jpg)An Azure DevOps portal (was VSTS Wiki) is the modern alternative to the 6 Word docs – see <br>      [Do you make instructions at the beginning of a project and improve them gradually?](/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=d6d34c31-ac6a-49a4-876a-f9d30e1ab78a)

### Unit Testing
![UnitTestExplorer.png](/PublishingImages/UnitTestExplorer.png)Figure: Nice Unit Tests explain what the code is supposed to be doing.![vs11debug.png](/PublishingImages/VS11Debug.png)Figure: Most young developers are happy with good old stepping through code with F11. The good thing is there are no diagrams that become out of date (which they always do after the first couple of sprints) giving you nasty Technical Debt.![tfspreviewbacklog.png](/PublishingImages/TFSPreviewBacklog.jpg)Figure: Don't forget that you have the completed requirements which get done and archived and can now serve as free documentation e.g. User Stories (aka PBIs)![Annotation and Comment](/PublishingImages/9c0cea_AnnotationAndComment.jpg)Figure: Annotations marry up the code with the PBIs, showing who, what, why and when for each piece of code

### Level 3+: The rest of the jigsaw


**Scrum Tip: Update your Acceptance Criteria** ​- If you subscribe to this work item check-in policy, then you understand that the PBI is now the documentation. If requirements change during the course of the PBI (based on a conversation with Product Owner of course) then the PBI should be updated.

When updating the acceptance criteria,        strike through the altered acceptance criteria and add the new ones. Get the PO to confirm your understanding.

E.g.
Enter search text, click ‘Google’, and see the results populate below.
[Updated]
Enter search text and automatically see the results populate below.

This should be added to the        [definition of done](/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=6449ae79-ba88-447e-aa48-36173029a2af).


![Technical Debt](/PublishingImages/Debt.jpg)
**What's "Technical Debt"?**

During a project, when you add functionality, you have a choice:

One way is quick but messy - it will make further changes harder in the future (i.e. quick and dirty).

The other way is cleaner – it will make changes easier to do in the future, but will take longer to put in place.

'Technical Debt' is a metaphor to help us think about this problem. In this metaphor (often mentioned during Scrum software projects), doing things the quick and dirty way gives us a 'technical debt', which will have to be fixed later. Like a financial debt, the technical debt incurs interest payments - in the form of the extra effort that we have to do in future development.

We can choose to continue paying the interest, or we can pay the debt up front by redoing the piece of work in the cleaner way.

The same principle is true with documentation. Using the 'old school' method will leave you with a build-up of documentation that you will need to keep up-to-date as the project evolves.

Warning: if you want to follow Scrum and have zero technical debt, then you have to throw away all documentation at the end of each sprint. If you do want to keep it, make sure you add it to your        [definition of done](/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=6449ae79-ba88-447e-aa48-36173029a2af)to keep it updated.


