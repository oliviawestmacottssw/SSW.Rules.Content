---
type: rule
archivedreason: 
title: Do you make awesome documentation?
guid: d9a17cdf-0f7c-43dc-91a1-7b8fcc29467d
uri: do-you-make-awesome-documentation
created: 2012-03-16T08:01:26.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
- title: Damian Brady
  url: https://ssw.com.au/people/damian-brady
- title: Eric Phan
  url: https://ssw.com.au/people/eric-phan
- title: Ulysses Maclaren
  url: https://ssw.com.au/people/ulysses-maclaren
- title: Adam Stephensen
  url: https://ssw.com.au/people/adam-stephensen
- title: Matt Goldman
  url: https://ssw.com.au/people/matt-goldman
related:
- reference-do-you-use-the-correct-symbols-when-documenting-instructions
- reference-do-you-use-the-right-order-of-instructions
- do-you-highlight-actions-correctly-in-your-document
- do-you-make-numbers-more-readable
- do-you-include-version-numbers-in-your-file
- do-you-refer-to-the-reader-and-author-consistently-throughout-your-document
- tiny-do-you-use-active-phrases-no-zombies-please
redirects: []

---



<p>​There are 2 styles of documentation&#58;<br></p>
<br><excerpt class='endintro'></excerpt><br>
<h3>Level 1 - Old School<br></h3><table class="ssw-rteTable-default" cellspacing="0" style="width&#58;80%;font-size&#58;1em;"><tbody><tr class="ssw-rteTableEvenRow-default"><th class="ssw-rteTableFirstCol-default">​<img class="ms-rteCustom-ImageArea" alt="IwS2" src="/PublishingImages/iwS2.jpg" style="margin-right&#58;10px;" /></th><td class="ssw-rteTableOddCol-default"><p>This team style does a lot of upfront documentation and planning, is very comfortable with Waterfall, and has rarely even heard of Agile &#58;)</p></td></tr></tbody></table><ul><li>Heavy, long documents<br></li><li>Sequence Diagrams</li><li>UML</li></ul><p>This is a well-established way to do documentation but the issue with it is that it gets out of date.</p><dl class="image"><dt> 
      <img alt="enterprisearchitect1" src="/PublishingImages/enterprisearchitect1.jpg" /> 
   </dt><dd>Figure&#58; Documentation can take the form of Sequence Diagrams</dd></dl><dl class="image"><dt> 
      <img alt="enterprisearchitectusecases.png" src="/PublishingImages/EnterpriseArchitectUseCases.jpg" /> 
   </dt><dd>Figure&#58; ...or Use Case Diagrams </dd></dl><p><b>Exception&#58;</b> Keep this limited to just enough documentation to cover a couple of sprints, and be committed to keeping it updated. The tool of choice if you're going down this road is Enterprise Architect (an excellent application built by Australians).</p><h3>Level 2 -&#160;Lots of documentation (and the 6 important documents)<br></h3><table class="ssw-rteTable-default" cellspacing="0" style="width&#58;80%;font-size&#58;1em;"><tbody><tr class="ssw-rteTableEvenRow-default"><th class="ssw-rteTableFirstCol-default">​<img class="ms-rteCustom-ImageArea" alt="Mark Zuckerberg" src="/PublishingImages/68843503-mark-zuckerberg.jpg" style="margin-right&#58;10px;" /></th><td class="ssw-rteTableLastCol-default">This team style are all under 30 and have never heard of FoxPro or Access<br></td></tr></tbody></table><p>6 small docs (a couple of pages max + in the order you would read them)&#58;</p><ul><li>Documentation\Business.docx - Explaining the business purpose of the app</li><li>Documentation\Instructions-Compile.docx - Contains instructions on 
      <a href="/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=d6d34c31-ac6a-49a4-876a-f9d30e1ab78a">how to get the project to compile (aka the F5 experience)</a></li><li>Documentation\Instructions-Deployment.docx - Describes the deployment process</li><li>Documentation\Patterns-and-Technologies.docx - Explaining the technical overview e.g. Broad architecture decisions, 3rd party utilities, patterns followed etc. (ie. SSW Data Onion)</li><li>Documentation\Definition-of-Done.docx – Ensures that your team 
      <a href="/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=6449ae79-ba88-447e-aa48-36173029a2af">maintains a high level of quality with a Definition of Done</a>​</li><li>Documentation\Definition-of-Ready.docx – Ensure that your PBIs are well defined before adding them to a sprint by specifying a 
      <a href="/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=637c230e-b1e3-4f2e-b2e0-c1a5431c1758">Definition of Ready</a></li><li>Unit Tests</li><li>Code and Work Items (Via the magic of Annotation)</li></ul><dl class="image"><dt> 
      <img alt="ProjectDocumentation.jpg" src="/PublishingImages/ProjectDocumentation.jpg" /> 
   </dt><dd>Figure&#58;&#160;6 small docs explain most of what you need to know very briefly<br></dd></dl><h3 class="ssw15-rteElement-H3">Level 3&#58; Go Markdown<br></h3><dl class="image"><dt> 
      <img src="/PublishingImages/vsts-wiki.jpg" alt="vsts-wiki.jpg" /> 
   </dt><dd>An Azure DevOps portal (was VSTS Wiki) is the modern alternative to the 6 Word docs – see 
      <a href="/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=d6d34c31-ac6a-49a4-876a-f9d30e1ab78a">Do you make instructions at the beginning of a project and improve them gradually?</a><br></dd></dl><h3 class="ssw15-rteElement-H3">Unit Testing</h3><dl class="image"><dt> 
      <img alt="UnitTestExplorer.png" src="/PublishingImages/UnitTestExplorer.png" /> 
   </dt><dd>Figure&#58; Nice Unit Tests explain what the code is supposed to be doing.</dd></dl><dl class="image"><dt> 
      <img alt="vs11debug.png" src="/PublishingImages/VS11Debug.png" /> 
   </dt><dd>Figure&#58; Most young developers are happy with good old stepping through code with F11. The good thing is there are no diagrams that become out of date (which they always do after the first couple of sprints) giving you nasty Technical Debt.</dd></dl><dl class="image"><dt> 
      <img alt="tfspreviewbacklog.png" src="/PublishingImages/TFSPreviewBacklog.jpg" /> 
   </dt><dd>Figure&#58; Don't forget that you have the completed requirements which get done and archived and can now serve as free documentation&#160;e.g. User Stories (aka PBIs)</dd></dl><dl class="image"><dt> 
      <img alt="Annotation and Comment" src="/PublishingImages/9c0cea_AnnotationAndComment.jpg" /> 
   </dt><dd>Figure&#58; Annotations marry up the code with the PBIs, showing who, what, why and when for each piece of code<br></dd></dl><h3>Level 3+&#58; The rest of the jigsaw</h3><div class="greyBox"><p>
      <b>Scrum Tip&#58; Update your Acceptance Criteria</b> ​- If you subscribe to this work item check-in policy, then you understand that the PBI is now the documentation. If requirements change during the course of the PBI (based on a conversation with Product Owner of course) then the PBI should be updated.</p><p>When updating the acceptance criteria, 
      <s>strike through</s> the altered acceptance criteria and add the new ones. Get the PO to confirm your understanding. 
      <br></p><p>E.g.<br><s>Enter search text, click ‘Google’, and see the results populate below.</s><br>[Updated]<br>Enter search text and automatically see the results populate below.</p><p>This should be added to the 
      <a href="/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=6449ae79-ba88-447e-aa48-36173029a2af">definition of done</a>.</p></div><div class="greyBox" style="margin-top&#58;20px;"> 
   <img class="ms-rteCustom-ImageArea" alt="Technical Debt" src="/PublishingImages/Debt.jpg" style="float&#58;right;" />
   <p>
      <strong>What's &quot;Technical Debt&quot;?</strong></p><p>During a project, when you add functionality, you have a choice&#58;</p><p>One way&#160;is quick but messy - it will make further changes harder in the future (i.e. quick and dirty).</p><p>The other way is cleaner – it will make changes easier to do in the future, but will take longer to put in place.</p><p>'Technical Debt' is a metaphor to help us think about this problem. In this metaphor (often mentioned during Scrum software projects), doing things the quick and dirty way gives us a 'technical debt', which will have to be fixed later. Like a financial debt, the technical debt incurs interest payments - in the form of the extra effort that we have to do in future development.</p><p>We can choose to continue paying the interest, or we can pay the debt up front by redoing the piece of work in the cleaner way.</p><p>The same principle is true with documentation. Using the 'old school' method will leave you with a build-up of documentation that you will need to keep up-to-date as the project evolves.</p><p>Warning&#58; if you want to follow Scrum and have zero technical debt, then you have to throw away all documentation at the end of each sprint. If you do want to keep it, make sure you add it to your 
      <a href="/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=6449ae79-ba88-447e-aa48-36173029a2af">definition of done </a>to keep it updated.</p></div>


