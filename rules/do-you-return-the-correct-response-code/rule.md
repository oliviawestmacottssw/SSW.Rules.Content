---
type: rule
title: Do you return the correct response code?
uri: do-you-return-the-correct-response-code
created: 2014-11-05T20:39:42.0000000Z
authors:
- id: 45
  title: Chris Briggs
- id: 38
  title: Drew Robson

---

The use of correct response codes is a simple yet crucial step, towards building a better WebAPI. By default, the WebAPI framework sets the response status code to 200 (OK), regardless if the task succeed or an error occurred.

You can **save yourself countless hours of painful debugging**, by specifying the correct response code.
 
For example: According to the HTTP/1.1 protocol, when a POST request results in the creation of a resource, the server should reply with status 201 (Created).

public Product PostProduct(Product item)
 {
 item = repository.Add(item);
 return item;
 }
Figure: Bad Example – By default a 200 status code is returned.
[ResponseType(typeof(CreditSnapshot))]
 public HttpResponseMessage PostProduct(Product item)
 {
 item = repository.Add(item);
 var response = Request.CreateResponse(HttpStatusCode.Created, item);

 return response;
 }
Figure: Good Example – When creating objects the “Created” status code is returned. 
​public void PutProduct(int id, Product product)
 {
     product.Id = id;
     if (!repository.Update(product))
     {
return Request.CreateResponse(HttpStatusCode.NotFound, ex.Message);
     }
 }
Figure: Good Example – When updating or deleting objects, if the object to be modified cannot be found throw exception with HttpStatusCode.NotFound ​
