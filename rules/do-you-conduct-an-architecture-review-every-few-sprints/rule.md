---
type: rule
archivedreason: 
title: Do you conduct an architecture review every few Sprints?
guid: f1401eba-50d4-4c6e-bb16-3959b9c2920c
uri: do-you-conduct-an-architecture-review-every-few-sprints
created: 2009-02-26T02:02:17.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
- title: Ulysses Maclaren
  url: https://ssw.com.au/people/ulysses-maclaren
- title: Cameron Shaw
  url: https://ssw.com.au/people/cameron-shaw
- title: Justin King
  url: https://ssw.com.au/people/justin-king
related: []
redirects: []

---



  <p>There are 2 main parts to any application. The UI which is what the customer can see and provide feedback on, and the underlying code which they really can't know if it is healthy or not.<br></p><p>Therefore it is important to conduct a '<a href="/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=7ba5e1cd-da39-4bf2-9fe2-5b899589b3d2">test please</a>' on the internal code and architecture of the application.</p><div>Ideally conduct a small 'Code + Architecture Review' for every sprint. Assuming a 2 week sprint, schedule a&#160;4 hour (2 architects x 2 hours) review.<br></div>

<br><excerpt class='endintro'></excerpt><br>

  <p>The following are items that are addressed in an architecture/code review&#58; </p>
<p><strong>Background information/overview of the project</strong> </p>
<ul>
    <li>Current system </li>
    <li>Objectives of the system </li>
    <li>Number of users (internal, external, edit, read only) </li>
    <li>Current technologies </li>
    <li>Current environment (SOA, SOE) </li>
</ul>
<p><strong>Points for discussion</strong> </p>
<ul>
    <li>Rich client </li>
    <li>Web client </li>
    <li>Smart client (any disconnected users?) </li>
    <li>Technology choices
    <ul>
        <li>Persistence layer (e.g. Database) </li>
        <li>Business layer </li>
        <li>UI </li>
        <li>Communications </li>
        <li>Workflow </li>
        <li>Integration - external systems </li>
    </ul>
    </li>
    <li>Requirements for 'package' software
    <ul>
        <li>PerformancePoint </li>
        <li>Reporting Services </li>
        <li>Accounting packages </li>
        <li>SharePoint </li>
    </ul>
    </li>
    <li>Usage Telemetry</li><li>Performance Monitoring</li><li>​Data migrations </li>
    <li>Data reporting </li>
    <li>User experience </li>
    <li>Network </li>
    <li>Responsibilities/players </li>
    <li>Infrastructure
    <ul>
        <li>Network </li>
        <li>Hardware </li>
    </ul>
    </li>
    <li>Deployment
    <ul>
        <li>Staged implementation </li>
        <li>In parallel </li>
        <li>Development/Test/Staging/Production </li>
    </ul>
    </li>
    <li>Disaster recovery </li>
    <li>Change control/source control </li>
    <li>Build Server </li>
    <li>Performance </li>
    <li>Scalability </li>
    <li>Extensibility </li>
    <li>Design patterns </li>
    <li>Maintainability </li>
    <li>Reliability (failover servers?) </li>
    <li>'Sellability' i.e. is the solution appropriate for the client? </li>
</ul>
<p><strong>Note&#58; If you are using Enterprise Architect, be aware of technical debt&#58;</strong></p>
<ul>
<li>Add a datetime of the last time the diagram was modified so we have an indication of when it is out of date</li>
<li>On your diagrams, be aware that some parts are done and some are not.</li>
</ul>



