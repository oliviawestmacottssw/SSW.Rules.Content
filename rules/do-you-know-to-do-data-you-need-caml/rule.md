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

 This field should not be null (Remove me when you edit this field). 



```
<Query>    <OrderBy>        <FieldRef Name="Modified" Ascending="FALSE"></FieldRef>    </OrderBy>    <Where>        <And>            <Neq>                <FieldRef Name="Status"></FieldRef>                <Value Type="Text">Completed</Value>            </Neq>            <IsNull>                <FieldRef Name="Sent"></FieldRef>            </IsNull>        </And>    </Where></Query>
```

Figure: Example of CAML query 
You can see - CAML is essentially the same as SQL WHERE syntax, but wrapped in an XML format.

Problems with CAML:

1. CAML is XML and is case sensitive – including attributes names. 

```
<Query>    <Where>        <Or>            <Eq>              <FieldRef name="Status" />             <Value Type="Text">Completed</Value>            </Eq>            <IsNull>                <FieldRef Name="Status" />            </IsNull>        </Or>    </Where></Query>
```

     Figure: Example of CAML query
2. SharePoint is not good at telling you if you made a mistake with your CAML query. ![](/Standards/SoftwareDevelopment/RulesToBetterSharePoint/PublishingImages/CAMLError.png)     Figure: Debug error message
3. Hard to debug.
Tips: Use 3rd Party tools - U2U CAML Query Builder <br>![](/Standards/SoftwareDevelopment/RulesToBetterSharePoint/PublishingImages/U2U.png)     Figure: U2U CAML Query Builder     Note: U2U CAML Builder is the best tool that we have. There are some occasional UI and interface issues, but for creating CAML and testing it against live SharePoint lists it gets the job done. And it’s FREE!






