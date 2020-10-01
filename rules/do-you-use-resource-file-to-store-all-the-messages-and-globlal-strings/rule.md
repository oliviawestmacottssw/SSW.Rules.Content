---
type: rule
title: Do you use resource file to store all the messages and globlal strings?
uri: do-you-use-resource-file-to-store-all-the-messages-and-globlal-strings
created: 2018-04-26T21:08:00.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

Storing all the messages and global strings in one place will make it easy to manage them and to keep the applications in the same style.

 ![Code_StoreMessage.jpg](Code_StoreMessage.jpg) Store messages in the Message.resx
Catch(SqlNullValueException sqlex)
{
Response.Write("The value cannot be null.");
}
Bad Example - if you want to change the message, it will cost you lots of time to investigate every try-catch block
Catch(SqlNullValueException sqlex)
{
Response.Write(GetGlobalResourceObject("Messages", "SqlValueNotNull"));
}
Better Example - better than the hard code, but still wordy

Catch(SqlNullValueException sqlex)
{
Response.Write(Resources.Messages.SqlValueNotNull); 'Good Code - storing message in resource file. 
}
Good Example
