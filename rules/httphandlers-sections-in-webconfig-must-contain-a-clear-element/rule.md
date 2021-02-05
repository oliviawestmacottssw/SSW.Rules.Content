---
type: rule
archivedreason: 
title: Do you know that 'httpHandlers' or 'httpModules' sections in web.config must contain a 'remove' or 'clear' element?
guid: 14359e59-b047-4e0b-aef5-f79ccd3eb373
uri: httphandlers-sections-in-webconfig-must-contain-a-clear-element
created: 2013-02-06T12:55:03.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
- title: Danijel Malik
  url: https://ssw.com.au/people/danijel-malik
related: []
redirects: []

---

If web.config contains a &lt;httpHandlers&gt; or &lt;httpModules&gt; section, that section must contain a &lt;remove... /&gt; or a &lt;clear /&gt; element.

This basically forces developers to explicitly enable inheritance in nested virtual directories. In 99% of cases this developers won't use inheritance on these two sections, however it causes issues when somebody wants to add a module or handler to the parent virtual directory.

<!--endintro-->


::: greybox


```
<configuration>
   <system.web>
      <httpHandlers>
         <add verb="*" 
              path="*.New" 
              type="MyHandler.New,MyHandler"/>
         <add verb="GET,HEAD" 
              path="*.MyNewFileExtension" 
              type="MyHandler.MNFEHandler,MyHandler.dll"/>
     </httpHandlers>
   <system.web>
</configuration>
```


:::
Figure: Bad example

::: greybox


```
<configuration>
   <system.web>
      <httpHandlers>
         <clear/>
         <add verb="*" 
              path="*.New" 
              type="MyHandler.New,MyHandler"/>
         <add verb="GET,HEAD" 
              path="*.MyNewFileExtension" 
              type="MyHandler.MNFEHandler,MyHandler.dll"/>
     </httpHandlers>
   <system.web>
<configuration>
```


:::
    Figure: Good example
