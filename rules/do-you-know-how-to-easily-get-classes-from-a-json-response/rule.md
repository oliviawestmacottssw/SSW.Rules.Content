---
type: rule
title: Do you know how to easily get classes from a JSON response?
uri: do-you-know-how-to-easily-get-classes-from-a-json-response
created: 2014-08-08T05:26:43.0000000Z
authors:
- id: 38
  title: Drew Robson

---

When integrating with external Web APIs which return a JSON response, there is a quick and easy way to generate classes to handle that response. 


Execute the request, and copy the text of the JSON response.

![8-08-2014-3-41-23-PM-compressor.png](8-08-2014-3-41-23-PM-compressor.png)

Create a new class in Visual Studio, and Click Edit | Paste Special | Past As JSON Classes and classes will be generated from the JSON in the clipboard.

![ Edit | Paste Special | Paste JSON As Classes](8-08-2014-3-53-17-PM-compressor.png)

![ Classes generated from the JSON](8-08-2014-3-56-34-PM-compressor.png)

The results may need cleaning up a little bit, but its much easier than trying to write them manually.
