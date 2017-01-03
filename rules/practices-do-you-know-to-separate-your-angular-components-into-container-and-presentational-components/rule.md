---
type: rule
archivedreason: 
title: Practices - Do you know to separate your Angular components into container and presentational components?
guid: 8beefebf-8aef-4821-b965-16c4a9923443
uri: practices-do-you-know-to-separate-your-angular-components-into-container-and-presentational-components
created: 2017-01-03T16:52:00.0000000Z
authors:
- title: Duncan Hunter
  url: https://ssw.com.au/people/duncan-hunter
- title: Gabriel George
  url: https://ssw.com.au/people/gabriel-george
related: []
redirects: []

---


<p class="ssw15-rteElement-P">​​​There are two types of components 'dumb' and 'smart' components. Dumb components normally have no dependencies and no logic and just have @Inputs() and @Outputs(). Smart components are their parent components that would have multiple dependencies and logic but not necessarily an HTML template.​<br></p>
<br><excerpt class='endintro'></excerpt><br>
<p class="ssw15-rteElement-P">​​Aiming to keep the components that display data 'dumb' makes them much easy to reuse in your application and less buggy, but many people do not like the terms smart and dumb components as a dumb component may just have less logic versus none. Many people and SSW included are preferring the terms container and presentational components for these reasons.​​​<br></p><p class="ssw15-rteElement-CodeArea"><b>company-list-table.component.ts</b><br>@Component(&#123;<br>&#160; &#160; selector&#58; 'fbc-company-list-table',<br>&#160; &#160; template&#58; `<br>&#160;&#160; &#160; &lt;table id=&quot;company-list-table&quot; class=&quot;table table-hover table-striped company-list-table-component&quot;&gt;<br>&#160; &#160; &#160; &#160; &#160; &#160; &lt;thead&gt;<br>&#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &lt;tr&gt;<br>&#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &lt;th&gt;Name&lt;/th&gt;<br>&#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &lt;th&gt;Phone&lt;/th&gt;<br>&#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &lt;th&gt;Email&lt;/th&gt;<br>&#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &lt;th&gt;&lt;/th&gt;<br>&#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &lt;/tr&gt;<br>&#160; &#160; &#160; &#160; &#160; &#160; &lt;/thead&gt;<br>&#160; &#160; &#160; &#160; &#160; &#160; &lt;tbody&gt;<br>&#160;&#160; &#160; &#160; &#160; &#160; &#160; &#160; &lt;tr class=&quot;item&quot; *ngFor=&quot;let company of companies&quot;&gt;<br>&#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &lt;td&gt;&#123;&#123;company.name&#125;&#125;&lt;/td&gt;<br>&#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &lt;td&gt;&#123;&#123;company.phone&#125;&#125;&lt;/td&gt;<br>&#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &lt;td&gt;&#123;&#123;company.email&#125;&#125;&lt;/td&gt;<br>&#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &lt;td class=&quot;button-column&quot;&gt;<br>&#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &lt;button routerLink=&quot;/company/detail/&#123;&#123;company.id&#125;&#125;&quot; class=&quot;btn btn-default&quot; &gt;Details&lt;/button&gt;<br>&#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &lt;button routerLink=&quot;/company/edit/&#123;&#123;company.id&#125;&#125;&quot; class=&quot;btn btn-default&quot; &gt;Edit&lt;/button&gt;<br>&#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &lt;button (click)=&quot;confirmDelete(company)&quot; class=&quot;btn btn-default&quot;&gt;Delete&lt;/button&gt;<br>&#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &lt;/td&gt;<br>&#160; &#160; &#160; &#160; &#160; &#160; &#160; &#160; &lt;/tr&gt;<br>&#160; &#160; &#160; &#160; &#160; &#160; &lt;/tbody&gt;<br>&#160; &#160; &#160; &#160; &lt;/table&gt;<br>&#160; &#160; `<br>&#125;)<br>export class CompanyListTableComponent &#123;<br>&#160; &#160; @Input() companies&#58; Company[] = [&lt;Company&gt;&#123;&#125;];<br>&#160; &#160; @Output() deleteCompanySelected = new EventEmitter&lt;number&gt;();<br>&#160; &#160; &#160; &#160; &#160; &#160; this.deleteCompanySelected.emit(company.id);<br>&#160; &#160; &#125;<br>&#125;</p><dd class="ssw15-rteElement-FigureGood">​Figure&#58; Good example of a presenta​​tional component with no injected dependencies​<br></dd>


