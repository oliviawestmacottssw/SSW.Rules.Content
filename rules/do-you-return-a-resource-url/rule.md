---
type: rule
title: Do you return a Resource URL?
uri: do-you-return-a-resource-url
created: 2014-11-05T18:22:22.0000000Z
authors:
- id: 24
  title: Adam Stephensen

---

When the Web API creates a resource, it should include the URI of the new resource in the Location header of the response.​
 
public Product PostProduct(Product item)
 {
 item = repository.Add(item);
 return item;
 } ​
Figure: Bad Example – The response does not contain a reference to the location of the new resource 
public HttpResponseMessage PostProduct(Product item)
 {
     item = repository.Add(item);
     var response = Request.CreateResponse(HttpStatusCode.Created, item);

      string uri = Url.Link("DefaultApi", new { id = item.Id });
     response.Headers.Location = new Uri(uri);
     return response;
 }
Figure: Good Example – The response message contains a link in the header to the created resource (and the “Created” status code is returned )​
