---
type: rule
title: Do you create a Sprint Review/Retro email?
uri: do-you-create-a-sprint-reviewretro-email
created: 2012-08-06T05:48:37.0000000Z
authors:
- id: 4
  title: Ulysses Maclaren
- id: 38
  title: Drew Robson
- id: 45
  title: Chris Briggs

---

 ​​After any Sprint Review and Retrospective, an email should be sent to all the stakeholders to update them on the outcome from the sprint:
 
- Subject: &lt;Client Name&gt; Sprint XX Review/Retro
- This is a reply to the <br>      [Sprint Forecast email](/Pages/Do-you-create-a-Sprint-Forecast-email.aspx)
- Screenshot of Burndown from Azure DevOps
- Breakdown of work completed (including current code coverage value)
- Link to test environment
- Relevant notes from the retrospective



Hi [Product Owner],


| Sprint in Review:  | [Sprint Number] |
| --- | --- |
| Sprint Goal:  | [Goal​] |
| Sprint Duration:  | [Numbe​r of weeks] |
| Project:  | [Project Name] |
| Project Portal:  | [Link to project Portal] |
| Test Environment:      | [Link to test environment] |
| Product Owner:  | [Product Owner Name] |


Attendees:        *(Optional as they may be in the to and CC)*

​

### Sprint Review





| **ID** | **Title** | **State** | ​**Effort**<br> |
| --- | --- | --- | --- |
| 24124 <br> | UI Improvements<br> | Done<br> | ​4<br> |
| 24112 <br> | Integrate Business Logic to MVC app  <br> | Done | ​8<br> |
| 24097 <br> | Styling<br> | Committed  <br> | ​16<br> |

Figure: Sprint Backlog from [Link to Sprint Backlog in Azure DevOps]


As per [https://rules.ssw.com.au/do-you-know-what-happens-at-a-sprint-retrospective-meeting​](/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=4f02d28d-5375-4530-abcb-0b541683bcbc), we review:

1. Sprint Burndown (a quick overview of the sprint)
![](/PublishingImages/burndown.JPG)Figure: Sprint Burndown
2. Code Coverage (hopefully tests are increasing each sprint)
XXX

3. Velocity        *(Optional)*
XXX

4. Burnup (for the release - the whole project, how are we tracking for the big picture?)
![Release Burnup.jpg](/PublishingImages/Release%20Burnup.jpg)Figure: Release Burnup
5. Production Deployments (How many times did we deploy to Production?)
![production-deploy.jpg](/PublishingImages/production-deploy.png)Figure: Deployments from Octopus Deploy
6​​. Application Health Overview Timeline (For the entire Sprint)​​

![Application Health Overview Timeline.png](/PublishingImages/Application%20Insights.jpg)

### ​Sprint Retrospective

As part of our commitment to inspect and adapt as a team we conduct a Sprint Retrospective at the end of every Sprint. Here are the results of our Sprint Retrospective:

**What went well?**
&lt;insert what went well from retro&gt;

**What didn’t go so well?**
&lt;insert what did not went well from retro&gt;

**What improvements will be made for the next Sprint?**
&lt;insert what improvements will be made for the next Sprint&gt;

**Definition of Ready *****- Optional***

&lt;insert the definition of Ready. Normally that the PBIs are Sized with Acceptance criteria added&gt;

**Definition of Done *****- Optional***

&lt;insert Definition of Done. Normally that it compiles, meets the acceptance criteria, and a test please has been sent if relevant&gt;​

&lt;This is as per the rule:        [https://rules.ssw.com.au/do-you-create-a-sprint-review-retro-email​](/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=2a845add-b4b9-45ac-b47f-c646fe7d0c40) /&gt;

Figure: Good Example - Template for Sprint Review/Retro Email. Subject: Sprint xxx Review/Retro
