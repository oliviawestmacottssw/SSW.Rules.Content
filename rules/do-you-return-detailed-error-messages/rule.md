---
type: rule
title: Do you return detailed error messages?
uri: do-you-return-detailed-error-messages
created: 2015-08-27T01:00:17.0000000Z
authors:
- id: 48
  title: Jeremy Cade

---

 
Good error design is as important to the sucess of an API as the API design itself. A good error message provides context and visibility on how to troubleshoot and resolve issues at critical times.
 
### Start by using the correct HTTP Status Codes.

The HTTP/1.1 RFC lists over 70 different HTTP Status Codes. Very few developers will be able to remember all of them, so it pays to keep it simple and use the most common Status Codes. The basic rule is to use the following three:

- **200 OK** - Everything worked. Success
- **400 Bad Request** - The consuming application did something wrong.
- **500 Internal Server Error** - The API Application did something wrong.


### Make your error messages as verbose as possible.

Error messages should contain a sufficient level of information that a developer or consuming client can act upon.

{
    "errorMessage": "An error has occurred."
}
Figure: Bad Example - The error message does not contain information that can be acted upon.
{
    "errorMessage": "Client ID is a required field. Please provide a Client ID."
}
Figure: Good Example - The error message provides explicit detail and a short description on how to fix the issue.
### Provide a Tracking or Correlation ID

A tracking or correlation ID will allows the consuming clients to provide the API developers with a reference point in their logs.

{
    "errorMessage": "An error has occurred. Please contact technical support"
}
Figure: Bad Example - No tracking or correlation ID is provided.
{
    "errorMessage": "An error has occurred. Please contact technical support",
    "errorId": "3022af02-482e-4c06-885a-81d811ce9b34"
}
Figure: Good Exmaple - A error ID is provided as part of the reponse.
### Provide an additional Help Resource

Providing a URI to an additional help resources as part of your request will allow consuming clients to find additional resources or documentation that relates to the defined problem.

`{
    "ErrorType": "DoesNotExist",
    "Id": "3022af02-482e-4c06-885a-81d811ce9b34",
    "Message": "No Client with a ID of 999999999 was found",
    "StatusCode": 404
}`
``Figure: Bad Example - No Help Link Provided

`{
    "ErrorType": "DoesNotExist",
    "HelpLink": "http://www.myapiapplication/api/help/doesnotexist",
    "Id": "3022af02-482e-4c06-885a-81d811ce9b34",
    "Message": "No Client with a ID of 999999999 was found",
    "StatusCode": 404
}`
Figure: Good Example - A help link is provided as part of the response.


