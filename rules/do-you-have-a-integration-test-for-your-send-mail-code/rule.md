---
type: rule
title: Do you have a integration test for your send mail code?
uri: do-you-have-a-integration-test-for-your-send-mail-code
created: 2020-03-12T20:42:54.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

 The code below shows how you could use TestSmtpServer to test your send mail code:​
 
​DotNetOpenMailProvider provider = new DotNetOpenMailProvider();
NameValueCollection configValue = new NameValueCollection();
configValue["smtpServer"] = "127.0.0.1";
configValue["port"] = "8081";
provider.Initialize("providerTest", configValue);
TestSmtpServer receivingServer = new TestSmtpServer();
try
{
 receivingServer.Start("127.0.0.1", 8081);
 provider.Send("phil@example.com", 
 "nobody@example.com", 
 "Subject to nothing", 
 "Mr. Watson. Come here. I need you.");
}
finally
{
 receivingServer.Stop();
}
// So Did It Work?
Assert.AreEqual(1, receivingServer.Inbox.Count);
ReceivedEmailMessage received = receivingServer.Inbox[0];
Assert.AreEqual("phil@example.com", received.ToAddress.Email);
Figure: This code could help you validate the send mail code​​

