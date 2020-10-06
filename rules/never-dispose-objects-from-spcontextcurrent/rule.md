---
type: rule
title: Never Dispose Objects from SPContext.Current
uri: never-dispose-objects-from-spcontextcurrent
created: 2013-08-29T00:36:26.0000000Z
authors:
- id: 9
  title: William Yin
- id: 34
  title: Brendan Richards

---

Disposing objects in SharePoint is important, but never do it with objects from SPContext.Current. SharePoint will manage disposing these objects itself.




**using** (SPWeb web =  **SPContext.Current.Site.RootWeb** )
{
 //do something here
}
Figure: Using statement is trying to dispose current site object - it will cause exception



Just simplely use "Current" object directly.

SPWeb web =  **SPContext.Current.Site.RootWeb** ;
//do something here
Figure: Use Current objects directly - don't need to dispose them
