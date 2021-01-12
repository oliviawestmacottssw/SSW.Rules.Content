---
type: rule
archivedreason: 
title: Do you version your .xml files?
guid: fe869a35-0ca6-4558-89ac-3e79ef775018
uri: do-you-version-your-xml-files
created: 2009-04-29T06:07:29.0000000Z
authors:
- title: Adam Cogan
  url: https://ssw.com.au/people/adam-cogan
- title: Ryan Tee
  url: https://ssw.com.au/people/ryan-tee
related: []
redirects: []

---

It is good to store program settings in an .xml file. But developers rarely worry about future schema changes and how they will inform the user it is an old schema.

 What is wrong with this?

<!--endintro-->


```
<?xml version="1.0" standalone="yes"?><br><NewDataSet><br>  <xs:schema id="NewDataSet" xmlns=""<br>     xmlns:xs="http://www.w3.org/2001/XMLSchema"<br>     xmlns:msdata="urn:schemas-microsoft-com:xml-msdata"><br>    <xs:element name=NewDataSet" msdata:IsDataSet="true" msdata:Locale="en-AU"><br>    <xs:complexType><br>      <xs:choice maxOccurs="unbounded"><br>       <xs:element name="Table1"><br>       <xs:complexType><br>       <xs:sequence><br>       <xs:element name="DateUpdated" type="xs:dateTime" minOccurs="0" /><br>       <xs:element name="NewDatabase" type="xs:boolean" minOccurs="0" /><br>       <xs:element name="ConnectionString" type="xs:string" minOccurs="0" /><br>       <xs:element name="SQLFilePath" type="xs:string" minOccurs="0" /><br>       <xs:element name="TimeOut" type="xs:int" minOccurs="0" /><br>       <xs:element name="TurnOnMSDE" type="xs:boolean" minOccurs="0" /><br>       <xs:element name="KeepXMLRecords" type="xs:boolean" minOccurs="0" /><br>       <xs:element name="UserMode" type="xs:boolean" minOccurs="0" /><br>       <xs:element name="ReconcileScriptsMode" type="xs:boolean" minOccurs="0" /><br>       <xs:element name="FolderPath" type="xs:string" minOccurs="0" /> /><br>       <xs:element name="SelectedFile" type="xs:string" minOccurs="0" /><br>       <xs:element name="UpdateVersionTable" type="xs:boolean" minOccurs="0" /><br>       </xs:sequence><br>       </xs:complexType><br>       </xs:element><br>      </xs:choice><br>     </xs:complexType><br>     </xs:element><br>    </xs:schema><br> <br>    <Table1><br>      <DateUpdated>2004-05-17T10:04:06.9438192+10:00</DateUpdated><br>      <NewDatabase>true</NewDatabase><br>      <ConnectionString>Provider=SQLOLEDB.1;Integrated Security=SSPI;<br>      Persist Security Info=False;<br>      Data Source=(local);Initial Catalog=master</ConnectionString><br>      <SQLFilePath>ver0001.sql</SQLFilePath><br>      <TimeOut>5</TimeOut><br>      <TurnOnMSDE>false</TurnOnMSDE><br>      <KeepXMLRecords>false</KeepXMLRecords><br>      <UserMode>true</UserMode><br>      <ReconcileScriptsMode>true</ReconcileScriptsMode><br>      <FolderPath>C:\Program Files\SSW SQL Deploy\Samples\DatabaseSQLScripts\<br>      </FolderPath><br>      <SelectedFile /><br>      <UpdateVersionTable>true</UpdateVersionTable><br>    </Table1><br></NewDataSet>
```

Bad example - XML file without version control. 

```
<?xml version="1.0" standalone="yes"?><br><NewDataSet><br>  <xs:schema id="NewDataSet" xmlns=""<br>     xmlns:xs="http://www.w3.org/2001/XMLSchema"<br>     xmlns:msdata="urn:schemas-microsoft-com:xml-msdata"><br>    <xs:element name=NewDataSet" msdata:IsDataSet="true" msdata:Locale="en-AU"><br>    <xs:complexType><br>      <xs:choice maxOccurs="unbounded"><br>       <xs:element name="Table1"><br>       <xs:complexType><br>       <xs:sequence><br>       <span style="background-color:rgb(255, 255, 0);"><xs:element name="Version" type="xs:string" minOccurs="0" /></span><br>       <xs:element name="DateUpdated" type="xs:dateTime" minOccurs="0" /><br>       <xs:element name="NewDatabase" type="xs:boolean" minOccurs="0" /><br>       <xs:element name="ConnectionString" type="xs:string" minOccurs="0" /><br>       <xs:element name="SQLFilePath" type="xs:string" minOccurs="0" /><br>       <xs:element name="TimeOut" type="xs:int" minOccurs="0" /><br>       <xs:element name="TurnOnMSDE" type="xs:boolean" minOccurs="0" /><br>       <xs:element name="KeepXMLRecords" type="xs:boolean" minOccurs="0" /><br>       <xs:element name="UserMode" type="xs:boolean" minOccurs="0" /><br>       <xs:element name="ReconcileScriptsMode" type="xs:boolean" minOccurs="0" /><br>       <xs:element name="FolderPath" type="xs:string" minOccurs="0" /> /><br>       <xs:element name="SelectedFile" type="xs:string" minOccurs="0" /><br>       <xs:element name="UpdateVersionTable" type="xs:boolean" minOccurs="0" /><br>       </xs:sequence><br>       </xs:complexType><br>       </xs:element><br>      </xs:choice><br>     </xs:complexType><br>     </xs:element><br>    </xs:schema><br> <br>   <Table1><br>      <span style="background-color:rgb(255, 255, 0);"><Version>1.2</Version></span> <br>      <DateUpdated>2004-05-17T10:04:06.9438192+10:00</DateUpdated><br>      <NewDatabase>true</NewDatabase><br>      <ConnectionString>Provider=SQLOLEDB.1;Integrated Security=SSPI;<br>      Persist Security Info=False;<br>      Data Source=(local);Initial Catalog=master</ConnectionString><br>      <SQLFilePath>ver0001.sql</SQLFilePath><br>      <TimeOut>5</TimeOut><br>      <TurnOnMSDE>false</TurnOnMSDE><br>      <KeepXMLRecords>false</KeepXMLRecords><br>      <UserMode>true</UserMode><br>      <ReconcileScriptsMode>true</ReconcileScriptsMode><br>      <FolderPath>C:\Program Files\SSW SQL Deploy\Samples\DatabaseSQLScripts\<br>      </FolderPath><br>      <SelectedFile /><br>      <UpdateVersionTable>true</UpdateVersionTable><br>    </Table1><br></NewDataSet>
```

Good example - XML file with version control 
The version tags identifies what version the file is. This version should be hard coded into the application. Every time you change the format of the file, you would increment this number.

The code below shows how this would be implemented in your project.


```
Public Function IsXMLFileValid() As Boolean<br><br>  Dim fileVersion As String = "not specified"<br>  Dim dsSettings As New DataSet<br>  Dim IsMalformed As Boolean = False <br>  ' Is the file malformed all together with possibly version<br><br>  Try<br>    dsSettings.ReadXml(mXMLFileInfo.FullName, XmlReadMode.ReadSchema)<br>  Catch ex As Exception<br>    IsMalformed = True<br>  End Try<br><br>  If (Not IsMalformed) Then<br>    Dim strm As Stream = Asm.GetManifestResourceStream(Asm.GetName().Name _ <br>     + "." + "XMLFileSchema.xsd")<br>    Dim sReader As New StreamReader(strm)<br>    Dim dsXMLSchema As New DataSet<br>    dsXMLSchema.ReadXmlSchema(sReader)<br><br>    If dsSettings.Tables(0).Columns.Contains("Version") Then _<br>      fileVersion = dsSettings.Tables(0).Rows(0)("Version").ToString<br>    End If<br><br>    If fileVersion = "" Then<br>      fileVersion = "not specified"<br>    End If<br><br>    If fileVersion = Global.XMLFileVersion AndAlso <br>        Not dsSettings.GetXmlSchema() = dsXMLSchema.GetXmlSchema() Then<br>      Return False<br>    End If<br><br>  End If<br><br>  If IsMalformed OrElse fileVersion <> Global.XMLFileVersion Then<br><br>    If mshouldConvertFile Then<br>      ' Convert the file<br>      ConvertToCurrentVersion(IsMalformed)<br>    Else<br>      Throw New XMLFileVersionException(fileVersion, Global.XMLFileVersion )<br>    End If<br><br>  End If<br><br>  Return True<br><br>End Function
```

**Figure: Code to illustrate how to check if the xml file is valid.** 
Note: to allow backward compatibility, you should give the user an option to convert old xml files into the new version structure.
