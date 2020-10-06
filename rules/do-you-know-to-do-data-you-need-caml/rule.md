---
type: rule
title: Do you know to do data you need CAML?
uri: do-you-know-to-do-data-you-need-caml
created: 2009-05-21T23:18:19.0000000Z
authors:
- id: 8
  title: John Liu
- id: 18
  title: Jay Lin

---

CAML is the XML definition for all things in SharePoint, in deployment, and in creating templates, CAML is the only format.
In SharePoint development, you will also need to know CAML, in particular, how to write a query in CAML.

- Widely used in Content Query Web Parts
- Also used in SharePoint content reports
- In code, used by SPSiteDataQuery object



[Introduction to Collaborative Application Markup Language (CAML)](http://msdn.microsoft.com/en-us/library/ms426449.aspx)
 


[Query Schema](http://msdn.microsoft.com/en-us/library/ms467521.aspx)







```
Completed
```

Figure: Example of CAML query 
You can see - CAML is essentially the same as SQL WHERE syntax, but wrapped in an XML format.

Problems with CAML:

1. CAML is XML and is case sensitive – including attributes names. 

```
name="Status" />             Completed                                        Name="Status" />
```

     Figure: Example of CAML query
2. SharePoint is not good at telling you if you made a mistake with your CAML query. 
![Debug error message](CAMLError.png)
3. Hard to debug.
Tips: Use 3rd Party tools - U2U CAML Query Builder<br>    
![U2U CAML Query BuilderNote: U2U CAML Builder is the best tool that we have. There are some occasional UI and interface issues, but for creating CAML and testing it against live SharePoint lists it gets the job done. And it’s FREE](U2U.png)!
