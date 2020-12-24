---
type: rule
archivedreason: 
title: Do you know how to use Connection String in .NET 2.0?
guid: 2dec2ea4-3359-4bb0-8f30-c278c8735670
uri: do-you-know-how-to-use-connection-string-in-net-20
created: 2009-05-08T08:53:04.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 17
  title: Ryan Tee
related: []
redirects: []

---

In .NET 1.1 we used to store our connection string in a configuration file like this:   
<!--endintro-->




```
<configuration><br>     <appsettings><br>          <add key="ConnectionString" value="integrated security=true;<br>           data source=(local);initial catalog=Northwind"></add><br>     </appsettings><br></configuration>
```


and access this connection string in code like this:


```
SqlConnection sqlConn = <br>new SqlConnection(System.Configuration.ConfigurationSettings.<br>AppSettings["ConnectionString"]);
```

Bad example - old ASP.NET 1.1 way, untyped and prone to error. 
In .NET 2.0 you can access it in another way

Step 1: Setup your settings in your common project. E.g. Northwind.Common

![Settings in Project Properties](ConnStringNET2_Settings.jpg)
Step 2: Open up the generated App.config under your common project. E.g. Northwind.Common/App.config

![Auto generated app.config](ConnStringNET2_CommonApp.GIF)
Step 3: ~~Copy the content into your entry applications app.config. E.g. Northwind.WindowsUI/App.config~~ The new setting has been updated to app.config automatically in .NET 2.0


```
<configuration><br>      <connectionstrings><br>         <add name="Common.Properties.Settings.NorthwindConnectionString"></add><br>              connectionString="Data Source=(local);Initial Catalog=Northwind;<br>              Integrated Security=True"<br>              providerName="System.Data.SqlClient" /><br>        </connectionstrings><br> </configuration>
```


Then you can access the connection string like this in C#


```
SqlConnection sqlConn =<br> new SqlConnection(Common.Properties.Settings.Default.NorthwindConnectionString);
```

Good example - access our connection string by strongly typed generated settings class. 

::: greybox

Please note these steps does not work for web site model in Visual Studio 2005. However, they work for other projects such as Windows Form, Console application, Class Library and Web Application Project.

This is not an issue in a well designed website, since it's connection string will be defined in the  **data layer** and you can overwrite this connection string in your web.config.

:::
