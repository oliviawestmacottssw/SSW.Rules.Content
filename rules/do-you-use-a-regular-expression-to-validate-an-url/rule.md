---
type: rule
title: Do you use a regular expression to validate an URL?
uri: do-you-use-a-regular-expression-to-validate-an-url
created: 2018-04-26T17:31:11.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

A regex is the best way to verify an URI.

 
public bool IsValidUri(string uri)
{
try 
{ 
Uri testUri = new Uri(uri); 
return true; 
} 
catch (UriFormatException ex)
{ 
return false; 
} 
}
Figure: Bad example of verifying URI​​​

public bool IsValidUri(string uri) 
{ 
// Return true if it is in valid Uri format.
return System.Text.RegularExpressions.Regex.IsMatch( uri,@"^(http|ftp|https)://([^\/][\w-/:]+\.?)+([\w- ./?/:/;/\%&=]+)?(/[\w- ./?/:/;/\%&=]\*)?"); 
}
 Figure: Good example of verifying URI 

You should have unit tests for it, see our [Rules to Better Unit Tests](https&#58;//www.ssw.com.au/ssw/Standards/Rules/RulesToBetterUnitTests.aspx) for more information.​
