---
layout: post
title:      "HTTP Verbs: Giving Requests a Function"
date:       2018-06-04 16:36:45 -0400
permalink:  http_verbs
---

HTTP verbs lend themselves to creating RESTful APIs whilst ensuring that all possible CRUD (Create, Read, Update, Delete) operations are present.

**HTTP GET**<br>
GET requests to *read* a resource without modifying it. GET requests do not therefore, change the state of the resource. It is said to be a safe method.

For any HTTP GET API, if the resource is found on the server, it will return the HTTP response code of 200 (accepted). If the resource is not found on the the server, it will return a 404 response whereby the resource could not be found. The HTTP response code of 400 will be returned if the GET request is not correctly formed; this is a bad request.

**HTTP POST**<br>
In relation to REST, the POST method *creates* a new resource into the collection of information. POST creates a new subordinate resource. 

Once a resource is created on the origin server, there are three likely HTTP response codes to follow. Response code 201 suggests that the resource was created. If the action performed by the POST request results in a resource that cannot be identified by a URI, HTTP response codes 200 or 204 are thrown. Responses to POST cannot typically be cached unless code stipulates otherwise. 

**HTTP PUT**<br>
PUT requests *update* existing resources, unless a resource does not exist, the API may create a new resource (or it may not). If the new resource is in fact created by the PUT request, the origin server must inform the user agent with the HTTP response code of 201 (created). If an existing resource is modified, either the 200 or 204 response is deployed; the latter of which suggests no content.

Reponses to this request cannot be cached.

**HTTP PATCH**<br>
PATCH is used for its modifying capabilities, and best corresponds to *update* in CRUD. The PATCH request only needs to contain the changes to the resource, not the complete resource.

PATCH is similar to PUT, but they are not interchangeable. POST requests are made of resource collections whereas PUT requests are made on individual resources. PUT also replaces the resource whereas PATCH applies a different resource.

**HTTP DELETE**<br>
DELETE requests will *delete* resources. HTTP responses to DELETE include, 200, 202 meaning the request has been queued or 204. Requesting DELETE on a resource is destructive and therefore cannot be called twice on a resource because a 404 error will be thrown. 

Responses to this method are not cacheable.





