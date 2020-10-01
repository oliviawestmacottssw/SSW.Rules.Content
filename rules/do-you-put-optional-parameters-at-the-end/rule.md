---
type: rule
title: Do you put optional parameters at the end?
uri: do-you-put-optional-parameters-at-the-end
created: 2018-04-26T23:44:44.0000000Z
authors:
- id: 1
  title: Adam Cogan

---

Optional parameters should be placed at the end of the method signature as optional ones tend to be less important. You should put the important parameters first.

 
public void SaveUserProfile(
[Optional] string username,
[Optional] string password,
string firstName,
string lastName, 
[Optional] DateTime? birthDate)
Figure: Bad Example - Username and Password are optional and first - they are less important than firstName and lastName and should be put at the end


public void SaveUserProfile(
string firstName,
string lastName, 
[Optional] string username,
[Optional] string password,
[Optional] DateTime? birthDate)
Figure: Good Example - All the optional parameters are the end


**Note:** When using optional parameters, please be sure to use [named para meters](/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=ba22dc4c-aec4-471d-8157-0a540ddf6310)
