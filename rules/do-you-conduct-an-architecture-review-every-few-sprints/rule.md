---
type: rule
title: Do you conduct an architecture review every few Sprints?
uri: do-you-conduct-an-architecture-review-every-few-sprints
created: 2009-02-26T02:02:17.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 4
  title: Ulysses Maclaren
- id: 2
  title: Cameron Shaw
- id: 5
  title: Justin King

---


There are 2 main parts to any application. The UI which is what the customer can see and provide feedback on, and the underlying code which they really can't know if it is healthy or not.

Therefore it is important to conduct a '[test please](http&#58;//www.ssw.com.au/SSW/Standards/Rules/RulestoSuccessfulProjects.aspx#TestPlease)' on the iinternal code and architecture of the application. 

 

Ideally conduct a small 'Code + Architecture Review' for every sprint. Assuming a 2 week sprint, schedule a 4 hour (2 architects x 2 hours) review during all sprints. 

The following are items that are address in a architecture/code review:

**Background information/overview of the project**

- Current system
- Objectives of the system
- Number of users (internal, external, edit, read only)
- Current technologies
- Current environment (SOA, SOE)


**Points for discussion**

- Rich client
- Web client
- Smart client (any disconnected users?)
- Technology choices
    - Persistence layer (SQL Server, Access, SQL Express, LINQ, netTiers)
    - Business layer
    - UI
    - Communications
    - Workflow
    - Integration - external systems
- Requirements for 'package' software
    - PerformancePoint
    - Reporting Services
    - Accounting packages
    - SharePoint
- Data migrations
- Data reporting
- User experience
- Network
- Responsibilities/players
- Infrastructure
    - Network
    - Hardware
- Deployment
    - Staged implementation
    - In parallel
    - Development/Test/Staging/Production
- Disaster recovery
- Change control/source control
- Build Server
- Performance
- Scalability
- Extensibility
- Design patterns
- Maintainability
- Reliability (failover servers?)
- 'Sellability' i.e. is the solution appropriate for the client?


**Enterprise Architect **

- should have a datetime of the last time the diagram was modified so we have an indication of when it is out of date
- should have the ability to mark items as ‘todo’. E.g. it would be nice to have an indication of which items on the diagrams have been completed, and which are still pending


