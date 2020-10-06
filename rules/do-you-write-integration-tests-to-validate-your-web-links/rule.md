---
type: rule
title: Do you write integration tests to validate your web links?
uri: do-you-write-integration-tests-to-validate-your-web-links
created: 2020-03-11T22:50:56.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

If you store your URL references in the application settings, you can create integration tests to validate them.
 
![URL for link stored in application settings](testURLSettings.gif)
**Sample Code: How to test the URL**

[Test]
 public void urlRulesToBetterInterfaces()
 {
 HttpStatusCode result = WebAccessTester.GetWebPageStatusCode(Settings.Default.urlRulesToBetterInterfaces);
 Assert.IsTrue(result == HttpStatusCode.OK, result.ToString());
 }

**Sample Code: Method used to verify the Page**

public class WebAccessTester
 {     
 public static HttpStatusCode GetWebPageStatusCode(string url)
 {
 HttpWebRequest req = ((HttpWebRequest)(WebRequest.Create(url)));
 req.Proxy = new WebProxy();
 req.Proxy.Credentials = CredentialCache.DefaultCredentials;
 HttpWebResponse resp = null;
 try
 {
 resp = ((HttpWebResponse)(req.GetResponse()));
 if (resp.StatusCode == HttpStatusCode.OK)
 {
 if (url.ToLower().IndexOf("redirect") == -1 && url.ToLower().IndexOf(resp.ResponseUri.AbsolutePath.ToLower()) == -1)
 {
 return HttpStatusCode.NotFound;
 }
 }
 }
 catch (System.Exception ex)
 {JavaScript
 while (!(ex == null))
 {
 Console.WriteLine(ex.ToString());
 Console.WriteLine("INNER EXCEPTION");
 ex = ex.InnerException;
 }
 }
 finally
 {
 if (!(resp == null))
 {
 resp.Close();
 }
 }
 return resp.StatusCode;
 }
 }
