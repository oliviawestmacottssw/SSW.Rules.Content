---
type: rule
title: Do you use MSAjax for Live Data Binding which saves round trips?
uri: do-you-use-msajax-for-live-data-binding-which-saves-round-trips
created: 2009-08-25T02:47:57.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

In old versions of ASP.NET AJAX the UI control couldn't get notification if the source had been changed. Developers had to write the extra code to refresh the value.

<br>In ASP.NET AJAX version 4.0, there is a new feature called "Live Data Binding", which means when there's any change in the data source, the changes are reflected to the data bound interface instantly and vice versa.  <br> **Binding Modes:**

- Sys.BindingMode.auto
<br>    This is the default binding mode. Two-way binding on an input control, and one-way binding on a context-type elements such as spans.<br>    

```
<b>Name: </b><input id="name" type="text" value="{binding name, mode=auto}" />
<b>Echo: </b><span id="nameDisplay">{binding name, mode=auto}</span>
```

Figure: When you update either textbox, the other one will be updated with the same value.
- Sys.BindingMode.twoWay
<br>    This is the default binding mode for input controls.<br>    

```
<b>Name: </b><input id="name" type="text" value="{binding name, mode=twoWay}" />
<b>Echo: </b><span id="nameDisplay">{binding name, mode=twoWay}</span>
```

Figure: When you update either textbox, the other one will be updated with the same value.
- Sys.BindingMode.oneWay <br>    

```
<b>Name: </b><input id="name" type="text" value="{binding name, mode=oneWay}" />
<b>Echo: </b><span id="nameDisplay">{binding name, mode=twoWay}</span>
```

Figure: When you update the Name, it won't affect the Echo.
- Sys.BindingMode.oneWayToSource


```
<b>Name: </b><input id="name" type="text" value="{binding name}" />
<b>Echo: </b><span id="nameDisplay">{binding name, mode=oneWayToSource}</span>
```

Figure: When you update the Name, it won't affect the Echo. But if you update Echo, it will affect the Name.
- Sys.BindingMode.oneTime<br>    

```
<b>Name: </b><input id="name" type="text" value="{binding name, mode=twoWay}" />
<b>Echo: </b><span id="nameDisplay">{binding name, mode=oneTime}</span>
```

Figure: When you update the Name in the first time, it will affect the Echo. After the first time, it won't affect the Echo.

 The live-binding syntax is similar to binding syntax in WPF (XAML).
