---
type: rule
archivedreason: 
title: Do you create a Sprint Review/Retro email?
guid: aac90a70-58a3-4b10-97a1-fef2dc6bda39
uri: do-you-create-a-sprint-review-retro-email
created: 2012-08-06T05:48:37.0000000Z
authors:
- title: Ulysses Maclaren
  url: https://ssw.com.au/people/ulysses-maclaren
- title: Drew Robson
  url: https://ssw.com.au/people/drew-robson
- title: Chris Briggs
  url: https://ssw.com.au/people/chris-briggs
related: []
redirects:
- do-you-create-a-sprint-reviewretro-email

---

After any Sprint Review and Retrospective, an email should be sent to all the stakeholders to update them on the outcome from the sprint:

<!--endintro-->

* Subject: <client name=""> Sprint XX Review/Retro </client>
* This is a reply to the <br>      [Sprint Forecast email](/Pages/Do-you-create-a-Sprint-Forecast-email.aspx)
* Screenshot of Burndown from Azure DevOps
* Breakdown of work completed (including current code coverage value)
* Link to test environment
* Relevant notes from the retrospective
* CC - SSWSprintReviews@sswcom.onmicrosoft.com



Hi [Product Owner],


| Sprint in Review:  | [Sprint Number] |
| --- | --- |
| Sprint Goal:  | [Goal] |
| Sprint Duration:  | [Number of weeks] |
| Project:  | [Project Name] |
| Project Portal:  | [Link to project Portal] |
| Test Environment:      | [Link to test environment] |
| Product Owner:  | [Product Owner Name] |


Attendees:        *(Optional as they may be in the to and CC)*



### Sprint Review





| **ID**  | **Title**  | **State**  |  **Effort** <br> |
| --- | --- | --- | --- |
| 24124 <br> | UI Improvements<br> | Done<br> | 4<br> |
| 24112 <br> | Integrate Business Logic to MVC app  <br> | Done | 8<br> |
| 24097 <br> | Styling<br> | Committed  <br> | 16<br> |

**Figure: Sprint Backlog from [Link to Sprint Backlog in Azure DevOps]** 


As per [https://rules.ssw.com.au/do-you-know-what-happens-at-a-sprint-retrospective-meeting](/RetrospectiveMeeting), we review:

1. Sprint Burndown (a quick overview of the sprint)
<dl class="image"><dt>
         <img src="burndown.JPG" alt="">
      </dt><dd>Figure: Sprint Burndown</dd></dl>
2. Code Coverage (hopefully tests are increasing each sprint)
XXX

3. Velocity        *(Optional)*
XXX

4. Burnup (for the release - the whole project, how are we tracking for the big picture?)
<dl class="image"><dt>
         <img alt="Release Burnup.jpg" src="Release Burnup.jpg" style="width:600px;">
      </dt><dd>Figure: Release Burnup</dd></dl>
5. Production Deployments (How many times did we deploy to Production?)
<dl class="image"><dt>
         <img alt="production-deploy.jpg" src="production-deploy.png" style="width:600px;">
      </dt><dd>Figure: Deployments from Octopus Deploy</dd></dl>
6. Application Health Overview Timeline (For the entire Sprint)


![](Application Insights.jpg)

### R&D 




**Did we do any experimental work?
**

<insert details="" of="" any="" trial/error="" processes,="" and="" ensure="" all="" detail="" is="" captured="" as="" per="" https://rules.ssw.com.au/do-you-record-your-failures=""><br></insert>

<insert details="" of="" any="" problems="" for="" which="" no="" solutions="" existed,="" and="" ensure="" detail="" is="" captured="" as="" per="" https://rules.ssw.com.au/do-you-record-your-research-under-the-pbi=""><br><br></insert>

### Sprint Retrospective


As part of our commitment to inspect and adapt as a team we conduct a Sprint Retrospective at the end of every Sprint. Here are the results of our Sprint Retrospective:

**What went well?** 
<insert what="" went="" well="" from="" retro=""><br></insert>

**What didn’t go so well?** 
<insert what="" did="" not="" went="" well="" from="" retro=""></insert>

**What improvements will be made for the next Sprint?** 
<insert what="" improvements="" will="" be="" made="" for="" the="" next="" sprint=""></insert>

**Definition of Ready** ***- Optional***

<insert the="" definition="" of="" ready.="" normally="" that="" the="" pbis="" are="" sized="" with="" acceptance="" criteria="" added=""></insert>

**Definition of Done** ***- Optional***

<insert definition="" of="" done.="" normally="" that="" it="" compiles,="" meets="" the="" acceptance="" criteria,="" and="" a="" test="" please="" has="" been="" sent="" if="" relevant=""></insert>

<this is="" as="" per="" the="" rule:=""></this>[https://rules.ssw.com.au/do-you-create-a-sprint-review-retro-email](/Do-you-create-a-Sprint-Review-email) />

**Figure: Good Example - Template for Sprint Review/Retro Email. Subject: Sprint xxx Review/Retro**
