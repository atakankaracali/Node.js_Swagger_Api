# Node.js_Swagger_Api

API Documentation Example using Swagger with Node.js

![swagger](https://user-images.githubusercontent.com/53658645/129714110-0c868de6-6ade-4cb6-a584-bdd3ac57d8d3.PNG)

API Documentation Procedures with Node.js Using Swagger

![ng1](https://user-images.githubusercontent.com/53658645/129714178-9164cdeb-3b0a-476f-919d-60472f677332.PNG)

The operations are as follows

![ng2](https://user-images.githubusercontent.com/53658645/129714207-edff4370-c5a9-4fb4-9290-18c7659cbc07.PNG)

Get and Post 

![ng3](https://user-images.githubusercontent.com/53658645/129714264-d108dd16-d76a-489f-a9fb-db3a3c98ecb7.PNG)

Update and Delete

200 OK

It indicates that the sent request has successfully completed its task. The things that will be returned in the body will vary depending on the request. If a GET request was sent, the requested resource will be sent in the body, if a HEAD request was sent, the requested information will be sent in the header, and if a POST request was sent, the result of the operation will be sent.

201 Created

If a resource is created at the client's request, a 201 code is returned. There are two important points here. A 201 is not returned before the resource is created. If this process will take a long time, a 202 Accepted code is returned.

202 Accepted

If the client's request will take time to be fulfilled and will continue asynchronously, it will be executed 202 times. However, this code does not guarantee successful expansion when the process is fulfilled. An error may also be given. Controllers use 202, but the use of other resources is not correct.

204 No Content

It is used to indicate that the server intentionally leaves the body field blank when no body is sent in response to the request sent by the client.

301 Moved Permanently

It indicates that the URI that the client sent the request to is no longer in use and is being served at another address. The new URI should be sent in the Location field in the header along with this code in the response.

304 Not Modified

This code is similar to 204. It is sent without a body. It indicates that the client already has the most up-to-date version of its source.

400 Bad Request

It is the general 4xx code. 400 is used when other codes do not meet our needs.

401 Unauthorized

Indicates that a protected resource is being accessed without the necessary authorization.

403 Forbidden

This code is often confused with 401, but the difference is that if authorization information was not sent at all or was sent incorrectly, 401 is returned, and if the authorization provided to the user does not have access to the requested resource, 403 is returned.

404 Not Found

Indicates that the resource requested by the client cannot be found.

405 Method Not Allowed

Indicates that the requested URI does not support the method in question. For example, if a POST request is sent to a resource that only has read permission, a 405 is returned.

406 Not Acceptable

It indicates that the server cannot provide output in any format from the media types written in the Accept field in the header of the request sent by the client. For example, if the Accept field of the request only contains application/json and the server cannot provide output in JSON type, 406 is returned.

409 Conflict

It indicates that the client is trying to put a resource on the server in a state that it should not be in with the request it sends. For example, if the client tries to make a non-nullable field null, 409 is returned.

415 Unsupported Media Type

When a resource of a type that is not supported is sent to the server, 415 is returned.

500 Internal Server Error

It is a general 5xx code, just like 400. It is used when the request cannot be fulfilled due to the server's error.
