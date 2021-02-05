---
type: rule
archivedreason: 
title: Do You Use a Dependency Injection Centric Architecture ?
guid: df1a3eca-21bb-4734-9276-18c0e1869be3
uri: do-you-use-a-dependency-injection-centric-architecture
created: 2012-10-19T19:11:41.0000000Z
authors:
- title: Adam Stephensen
  url: https://ssw.com.au/people/adam-stephensen
- title: Igor Goldobin
  url: https://ssw.com.au/people/igor-goldobin
related: []
redirects: []

---


<img class="ms-rteCustom-ImageArea" alt="inject" src="dependency-injection-bad.jpg" /> <span class="ms-rteCustom-FigureBad">Figure: Bad Example – N-Tiered architectures do not inherently support dependency injection</span> <img class="ms-rteCustom-ImageArea" alt="inject" src="dependency-injection-good.jpg" /> <span class="ms-rteCustom-FigureGood">Figure: Good Example – The Onion Architecture promotes layers built on interfaces, and then injecting dependencies into those layers. This keeps coupling low, and therefore maintainability high</span> 
<br><excerpt class='endintro'></excerpt><br>
<p>The classes in each layer can depend on layers toward the centre.</p><p>It emphasizes the use of interfaces for the business logic and repository layers. The repository layer corresponds to the Data Access layer in an n-Tier architecture.</p><p>An n-Tier architecture has at its base the database.<br>The core of the onion architecture is the Domain Model, and all dependencies are injected. This leads to more ​maintainable applications since it emphasizes separation of concerns.</p>
<h4> Further Reading: </h4><ul><li>
      <a href="/Pages/The-layers-of-the-onion-architecture.aspx">Do you know the layers of the onion architecture?</a></li><li>
      <a href=/do-you-know-the-best-dependency-injection-container-aka-do-not-waste-days-evaluating-ioc-containers>Do you know the best dependency injection container​?​</a></li></ul>


