---
type: rule
title: Do you send "Sprint Forecast" and "Sprint Review/Retro" emails to the client?
uri: do-you-send-sprint-forecast-and-sprint-reviewretro-emails-to-the-client
created: 2009-08-18T05:22:13.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 4
  title: Ulysses Maclaren

---

 
Each sprint has a "Sprint Forecast" email that details what will be worked on during this sprint.

At the end of the sprint, this should be replied to with a "Sprint Review" email that shows a breakdown of what was completed.

Each sprint has the following stages:

1. Planning meeting:
    - Sprint Forecast email
    - See [http://rules.ssw.com.au/Management/RulesToBetterScrumUsingTFS/Pages/Do-you-have-a-Sprint-Contract-aka-The-deal-between-the-Product-Owner-and-Team.aspx](/Management/RulesToBetterScrumUsingTFS/Pages/Do-you-have-a-Sprint-Contract-aka-The-deal-between-the-Product-Owner-and-Team.aspx) for more details
2. Review and Retro meetings
    - The Sprint review/retro email: "Northwind Sprint 5 Review/Retro"
        - Subject: Sprint xxx Review
        - This is a reply to the Sprint Plan email
        - Breakdown of work completed
        - Screenshot of Burndown
        - Link to test environment
        - Relevant notes from the retro

Hi Mr Northwind 

Here is an update: 

- currently working on **Northwind Release\_10\_Jobs**
- I did a build on Friday see http://ant:8000/Northwind/
    - Status: Internal Test Failed
- % of Tasks Done:  62% complete
    - http://tfs.northwind.com/XXX
- Budget used:          60% used 
    - Authorized:  $75,000
    - Spent:          $39,715
- I expect to finish on Fri 30/05/2008


Regards Eric Figure: The above is a sample of the "Sprint XXX Review/Retro" email 
