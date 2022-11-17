# 301 Class Eight Reading Notes "APIs"

Most modern web applications expose APIs that clients can use to interact with the application. A well-designed web API should aim to support:

- Platform independence. Any client should be able to call the API, regardless of how the API is implemented internally. This requires using standard protocols, and having a mechanism whereby the client and the web service can agree on the format of the data to exchange.

- Service evolution. The web API should be able to evolve and add functionality independently from client applications. As the API evolves, existing client applications should continue to function without modification. All functionality should be discoverable so that client applications can fully use it.

This guidance describes issues that you should consider when designing a web API.

## What is REST?

In 2000, Roy Fielding proposed Representational State Transfer (REST) as an architectural approach to designing web services. REST is an architectural style for building distributed systems based on hypermedia. REST is independent of any underlying protocol and is not necessarily tied to HTTP. However, most common REST API implementations use HTTP as the application protocol, and this guide focuses on designing REST APIs for HTTP.

A primary advantage of REST over HTTP is that it uses open standards, and does not bind the implementation of the API or the client applications to any specific implementation. For example, a REST web service could be written in ASP.NET, and client applications can use any language or toolset that can generate HTTP requests and parse HTTP responses.

## Questions

1. What does REST stand for?  Representational State Transfer
2. REST APIs are designed around resources which is any kind of object data.
3. What is an identifier of a resource? Give an example. `https://adventure-works.com/orders/1` is an example of a URI that identifies a resource.
4. What are the most common HTTP verbs? GET POST PUT PATCH DELETE
5. What should the URIs be based on? when possible they should be based on nouns
6. Give an example of a good URI. `https://adventure-works.com/orders`
7. What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing? a chatty API is a bad thing and has many requests for data
8. What status code does a successful GET request return? 200
9. What status code does an unsuccessful GET request return? 404
10. What status code does a successful POST request return? 201
11. What status code does a successful DELETE request return? 204

## Resources

[APIs](https://learn.microsoft.com/en-us/azure/architecture/best-practices/api-design)

## Return to the Table of Contents

[Table of Contents](https://todd75.github.io/reading-notes/)
