---
type: rule
title: Do you know that 'httpHandlers' or 'httpModules' sections in web.config must contain a 'remove' or 'clear' element?
uri: do-you-know-that-httphandlers-or-httpmodules-sections-in-webconfig-must-contain-a-remove-or-clear-element
created: 2013-02-06T12:55:03.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 46
  title: Danijel Malik

---

If web.config contains a &lt;httpHandlers&gt; or &lt;httpModules&gt; section, that section must contain a &lt;remove... /&gt; or a &lt;clear /&gt; element.

This basically forces developers to explicitly enable inheritance in nested virtual directories. In 99% of cases this developers won't use inheritance on these two sections, however it causes issues when somebody wants to add a module or handler to the parent virtual directory.
 
[[greyBox | Bad example]]
|  
| 
| ```
| <configuration>
|    <system.web>
|       <httpHandlers>
|          <add verb="*" 
|               path="*.New" 
|               type="MyHandler.New,MyHandler"/>
|          <add verb="GET,HEAD" 
|               path="*.MyNewFileExtension" 
|               type="MyHandler.MNFEHandler,MyHandler.dll"/>
|      </httpHandlers>
|    <system.web>
| </configuration>
| ```
| 
|
[[greyBox | Good example]]
|  
| 
| ```
| <configuration>
|    <system.web>
|       <httpHandlers>
|          <clear/>
|          <add verb="*" 
|               path="*.New" 
|               type="MyHandler.New,MyHandler"/>
|          <add verb="GET,HEAD" 
|               path="*.MyNewFileExtension" 
|               type="MyHandler.MNFEHandler,MyHandler.dll"/>
|      </httpHandlers>
|    <system.web>
| <configuration>
| ```
| 
|
