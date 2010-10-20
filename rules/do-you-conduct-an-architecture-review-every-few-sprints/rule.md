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


An internal architecture review is the application of the [Test Please](/Management/RulesToSuccessfulProjects/Pages/InternalTestPlease.aspx) principle against the design phase. An architecture review conducted during every release minimises errors in design which saves future recitification costs.

Schedule a 4 hour (2 architects x 2 hours) review during all releases. While it may not be so important to conduct a review in every development release, they are compulsory for a specification release.

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
    - Persistance layer (SQL Server, Access, SQL Express, LINQ, netTiers)
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


